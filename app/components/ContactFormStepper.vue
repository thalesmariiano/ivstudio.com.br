<script setup lang="ts">
type ServiceOption = 'site' | 'identidade' | 'outro'

const CONTACT_EMAIL = 'contato@ivstudio.com.br'

const step = ref<0 | 1 | 2>(0)

const form = reactive({
  service: null as ServiceOption | null,
  otherService: '',
  name: '',
  email: '',
  whatsapp: '',
  message: '',
})

const attemptedNext = ref(false)
const submitted = ref(false)

const serviceLabel = computed(() => {
  if (form.service === 'site') return 'Quero criar um site'
  if (form.service === 'identidade') return 'Quero uma identidade visual'
  if (form.service === 'outro') return 'Outro'
  return ''
})

function isValidEmail(email: string) {
  return /^[^\s@]+@[^\s@]+\.[^\s@]+$/.test(email.trim())
}

function isValidWhatsapp(value: string) {
  const digits = value.replace(/\D/g, '')
  return digits.length >= 10 && digits.length <= 13
}

const stepValid = computed(() => {
  if (step.value === 0) {
    if (!form.service) return false
    if (form.service === 'outro') return form.otherService.trim().length >= 3
    return true
  }

  if (step.value === 1) {
    if (form.name.trim().length < 2) return false
    if (!isValidEmail(form.email)) return false
    if (!isValidWhatsapp(form.whatsapp)) return false
    return true
  }

  if (step.value === 2) {
    return form.message.trim().length >= 10
  }

  return false
})

const progress = computed(() => ((step.value + 1) / 3) * 100)

function goBack() {
  attemptedNext.value = false
  submitted.value = false
  if (step.value > 0) step.value = (step.value - 1) as 0 | 1 | 2
}

function goNext() {
  attemptedNext.value = true
  if (!stepValid.value) return
  attemptedNext.value = false
  if (step.value < 2) step.value = (step.value + 1) as 0 | 1 | 2
}

function buildEmailBody() {
  const lines = [
    `Serviço: ${serviceLabel.value}${form.service === 'outro' ? ` (${form.otherService.trim()})` : ''}`,
    `Nome: ${form.name.trim()}`,
    `E-mail: ${form.email.trim()}`,
    `WhatsApp: ${form.whatsapp.trim()}`,
    '',
    'Mensagem:',
    form.message.trim(),
  ].filter(Boolean) as string[]

  return lines.join('\n')
}

function submit() {
  attemptedNext.value = true
  if (!stepValid.value) return

  const subject = encodeURIComponent('Contato - IV Studio')
  const body = encodeURIComponent(buildEmailBody())
  const to = CONTACT_EMAIL

  submitted.value = true
  attemptedNext.value = false

  if (process.client) {
    window.location.href = `mailto:${to}?subject=${subject}&body=${body}`
  }
}
</script>

<template>
  <div class="w-full max-w-xl mx-auto">
    <div class="w-full rounded-3xl bg-[rgb(32,32,32)] border border-white/10 p-5 xs:p-7">
      <div class="space-y-4">
        <div class="flex items-center justify-between">
          <span class="font-poppins font-light text-white/80 text-sm tracking-[2px] uppercase">
            Etapa {{ step + 1 }} de 3
          </span>
          <span class="font-poppins font-light text-white/70 text-sm">
            {{ Math.round(progress) }}%
          </span>
        </div>

        <div class="w-full h-2 rounded-full bg-black/40 overflow-hidden">
          <div
            class="h-full bg-gradient-to-r from-neutral-200 to-neutral-500 transition-[width] duration-300"
            :style="{ width: `${progress}%` }"
          />
        </div>
      </div>

      <form class="mt-7 space-y-7" @submit.prevent="step === 2 ? submit() : goNext()">
        <div v-if="step === 0" class="space-y-4">
          <div class="space-y-2">
            <h2 class="font-poppins font-semibold text-white text-xl">Como podemos te ajudar?</h2>
            <p class="font-poppins font-light text-white/80">
              Selecione a opção que mais se encaixa no que você precisa agora.
            </p>
          </div>

          <fieldset class="space-y-3">
            <legend class="sr-only">Selecione o serviço</legend>

            <label
              class="block rounded-2xl border p-4 cursor-pointer transition-colors"
              :class="form.service === 'site' ? 'border-white/40 bg-white/5' : 'border-white/10 hover:border-white/20'"
            >
              <input v-model="form.service" class="sr-only" type="radio" name="service" value="site" />
              <div class="flex items-center justify-between gap-3">
                <div class="space-y-1">
                  <div class="font-poppins font-medium text-white">Quero criar um site</div>
                  <div class="font-poppins font-light text-white/70 text-sm">Landing page, site institucional, e-commerce.</div>
                </div>
                <div
                  class="w-4 h-4 rounded-full border"
                  :class="form.service === 'site' ? 'bg-white border-white' : 'border-white/40'"
                />
              </div>
            </label>

            <label
              class="block rounded-2xl border p-4 cursor-pointer transition-colors"
              :class="form.service === 'identidade' ? 'border-white/40 bg-white/5' : 'border-white/10 hover:border-white/20'"
            >
              <input v-model="form.service" class="sr-only" type="radio" name="service" value="identidade" />
              <div class="flex items-center justify-between gap-3">
                <div class="space-y-1">
                  <div class="font-poppins font-medium text-white">Quero uma identidade visual</div>
                  <div class="font-poppins font-light text-white/70 text-sm">Logo, paleta, tipografia e aplicações.</div>
                </div>
                <div
                  class="w-4 h-4 rounded-full border"
                  :class="form.service === 'identidade' ? 'bg-white border-white' : 'border-white/40'"
                />
              </div>
            </label>

            <label
              class="block rounded-2xl border p-4 cursor-pointer transition-colors"
              :class="form.service === 'outro' ? 'border-white/40 bg-white/5' : 'border-white/10 hover:border-white/20'"
            >
              <input v-model="form.service" class="sr-only" type="radio" name="service" value="outro" />
              <div class="flex items-center justify-between gap-3">
                <div class="space-y-1">
                  <div class="font-poppins font-medium text-white">Outro</div>
                  <div class="font-poppins font-light text-white/70 text-sm">Me conte rapidamente o que você precisa.</div>
                </div>
                <div
                  class="w-4 h-4 rounded-full border"
                  :class="form.service === 'outro' ? 'bg-white border-white' : 'border-white/40'"
                />
              </div>
            </label>

            <div v-if="form.service === 'outro'" class="pt-1">
              <label class="block space-y-2">
                <span class="font-poppins font-light text-white/80 text-sm">Qual é a sua necessidade?</span>
                <input
                  v-model="form.otherService"
                  class="w-full rounded-xl bg-black/30 border border-white/10 px-4 py-3 font-poppins text-white placeholder:text-white/40 outline-none focus:border-white/30"
                  type="text"
                  autocomplete="off"
                  placeholder="Ex.: social media, design para campanha, etc."
                />
              </label>
            </div>

            <p v-if="attemptedNext && step === 0 && !stepValid" class="font-poppins text-sm text-red-300">
              Selecione uma opção (e preencha o “Outro”, se necessário) para continuar.
            </p>
          </fieldset>
        </div>

        <div v-else-if="step === 1" class="space-y-4">
          <div class="space-y-2">
            <h2 class="font-poppins font-semibold text-white text-xl">Seus dados</h2>
            <p class="font-poppins font-light text-white/80">
              Assim a gente consegue te responder com mais rapidez.
            </p>
          </div>

          <div class="grid grid-cols-1 sm:grid-cols-2 gap-4">
            <label class="block space-y-2">
              <span class="font-poppins font-light text-white/80 text-sm">Nome</span>
              <input
                v-model="form.name"
                class="w-full rounded-xl bg-black/30 border border-white/10 px-4 py-3 font-poppins text-white placeholder:text-white/40 outline-none focus:border-white/30"
                type="text"
                autocomplete="name"
                placeholder="Seu nome"
              />
            </label>

            <label class="block space-y-2">
              <span class="font-poppins font-light text-white/80 text-sm">E-mail</span>
              <input
                v-model="form.email"
                class="w-full rounded-xl bg-black/30 border border-white/10 px-4 py-3 font-poppins text-white placeholder:text-white/40 outline-none focus:border-white/30"
                type="email"
                autocomplete="email"
                inputmode="email"
                placeholder="voce@exemplo.com"
              />
            </label>

            <label class="block space-y-2 sm:col-span-2">
              <span class="font-poppins font-light text-white/80 text-sm">WhatsApp</span>
              <input
                v-model="form.whatsapp"
                class="w-full rounded-xl bg-black/30 border border-white/10 px-4 py-3 font-poppins text-white placeholder:text-white/40 outline-none focus:border-white/30"
                type="tel"
                autocomplete="tel"
                inputmode="tel"
                required
                placeholder="(xx) xxxxx-xxxx"
              />
            </label>
          </div>

          <p v-if="attemptedNext && step === 1 && !stepValid" class="font-poppins text-sm text-red-300">
            Preencha nome, um e-mail válido e um WhatsApp válido para continuar.
          </p>
        </div>

        <div v-else class="space-y-4">
          <div class="space-y-2">
            <h2 class="font-poppins font-semibold text-white text-xl">Conte um pouco mais</h2>
            <p class="font-poppins font-light text-white/80">
              Quanto mais contexto, melhor o orçamento e o prazo.
            </p>
          </div>

          <label class="block space-y-2">
            <span class="font-poppins font-light text-white/80 text-sm">Mensagem</span>
            <textarea
              v-model="form.message"
              class="w-full min-h-32 rounded-xl bg-black/30 border border-white/10 px-4 py-3 font-poppins text-white placeholder:text-white/40 outline-none focus:border-white/30 resize-y"
              placeholder="Ex.: objetivo do projeto, referências, prazo, páginas, funcionalidades..."
            />
          </label>

          <p v-if="attemptedNext && step === 2 && !stepValid" class="font-poppins text-sm text-red-300">
            Escreva uma mensagem com pelo menos 10 caracteres.
          </p>

          <p v-if="submitted" class="font-poppins text-sm text-emerald-200">
            Perfeito — abrindo seu app de e-mail para enviar a mensagem.
          </p>
        </div>

        <div class="flex flex-col sm:flex-row sm:items-center sm:justify-between gap-3 pt-2">
          <button
            type="button"
            class="w-full sm:w-auto px-5 py-3 rounded-xl border border-white/15 text-white font-poppins font-medium hover:border-white/25 transition-colors disabled:opacity-40 disabled:hover:border-white/15"
            :disabled="step === 0"
            @click="goBack"
          >
            Voltar
          </button>

          <button
            v-if="step < 2"
            type="button"
            class="w-full sm:w-auto px-6 py-3 rounded-xl bg-gradient-to-r from-neutral-200 to-neutral-500 text-black font-poppins font-semibold hover:brightness-110 transition-[filter] disabled:opacity-50 disabled:hover:brightness-100"
            :disabled="attemptedNext && !stepValid"
            @click="goNext"
          >
            Avançar
          </button>

          <button
            v-else
            type="submit"
            class="w-full sm:w-auto px-6 py-3 rounded-xl bg-gradient-to-r from-neutral-200 to-neutral-500 text-black font-poppins font-semibold hover:brightness-110 transition-[filter]"
          >
            Enviar
          </button>
        </div>
      </form>
    </div>
  </div>
</template>

