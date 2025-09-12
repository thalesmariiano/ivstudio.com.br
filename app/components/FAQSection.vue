<template>
    <section
        class="w-full bg-[url('@/assets/images/start-bg.png')] bg-position-[7rem_5rem] bg-no-repeat bg-black px-5 sm:px-10 py-20">

        <h1 class="font-poppins font-semibold italic text-white text-center text-lg mb-7">// Dúvidas? Nós temos as
            respostas</h1>

        <div class="flex flex-col items-center">
            <Accordion accordion-id="acc-1">
                <template #question>
                    Quanto tempo leva para meu site ficar pronto?
                </template>
                <template #answer>
                    O prazo varia conforme a complexidade do projeto. Sites mais simples podem ficar prontos em 10 a 20
                    dias úteis, enquanto projetos mais completos podem levar de 30 a 45 dias. Sempre alinhamos o
                    cronograma com você antes de começar.
                </template>
            </Accordion>
            <Accordion accordion-id="acc-2">
                <template #question>
                    Meu site será responsivo para celular e tablet?
                </template>
                <template #answer>
                    Sim! Todos os sites que desenvolvemos já são 100% responsivos, ou seja, se adaptam automaticamente a
                    diferentes telas — celular, tablet e computador.
                </template>
            </Accordion>
            <Accordion accordion-id="acc-3">
                <template #question>
                    Posso solicitar alterações no design durante o processo?
                </template>
                <template #answer>
                    Claro! Você pode sugerir ajustes em pontos específicos durante as etapas de aprovação. Nosso
                    objetivo é entregar um resultado que esteja de acordo com sua visão e estratégia.
                </template>
            </Accordion>
            <Accordion accordion-id="acc-4">
                <template #question>
                    Quanto custa para criar um site?
                </template>
                <template #answer>
                    Não existe um valor fixo, pois cada projeto é único. O custo depende do tipo de site,
                    funcionalidades, design e prazos. Fazemos um orçamento personalizado de acordo com a sua
                    necessidade.
                </template>
            </Accordion>
            <Accordion accordion-id="acc-5">
                <template #question>
                    Depois de pronto, preciso pagar alguma mensalidade?
                </template>
                <template #answer>
                    O investimento inicial cobre o desenvolvimento e a entrega do site. A única mensalidade que você
                    terá é referente à hospedagem e domínio, pagos diretamente à empresa contratada. Caso precise de
                    suporte contínuo, oferecemos planos opcionais.
                </template>
            </Accordion>
            <Accordion accordion-id="acc-6">
                <template #question>
                    Vocês oferecem manutenção ou suporte após a entrega?
                </template>
                <template #answer>
                    Sim! Temos planos de manutenção e suporte que incluem atualizações, ajustes e monitoramento, para
                    manter seu site seguro e sempre funcionando bem.
                </template>
            </Accordion>
            <Accordion accordion-id="acc-7">
                <template #question>
                    Eu preciso fornecer todo o conteúdo ou vocês criam tudo?
                </template>
                <template #answer>
                    Você pode fornecer os textos, imagens e materiais que já tiver. Mas, se preferir, nossa equipe pode
                    auxiliar na criação de conteúdo, imagens e até no refinamento do texto, para deixar o site mais
                    profissional.
                </template>
            </Accordion>
        </div>
    </section>
</template>