<template>
    <section class="w-full bg-[url('@/assets/images/start-bg.png')] bg-position-[7rem_5rem] bg-no-repeat bg-black px-5 sm:px-10 py-20">
        
        <h1 class="font-poppins font-semibold italic text-white text-center text-lg mb-7">// Dúvidas? Nós temos as respostas</h1>

        <div class="flex flex-col items-center">
            <Accordion accordion-id="acc-1">
                <template #question>
                    Quanto tempo leva para meu site ficar pronto?
                </template>
                <template #answer>
                    Lorem, ipsum dolor sit amet consectetur adipisicing elit. Porro inventore repellendus fugit deserunt ipsum sit dolor ab unde nostrum ullam numquam nam illo ex quis accusantium iusto, laudantium voluptatum minima!
                </template>
            </Accordion>
            <Accordion accordion-id="acc-2">
                <template #question>
                    Meu site será responsivo para celular e tablet?
                </template>
                <template #answer>
                    Lorem, ipsum dolor sit amet consectetur adipisicing elit. Porro inventore repellendus fugit deserunt ipsum sit dolor ab unde nostrum ullam numquam nam illo ex quis accusantium iusto, laudantium voluptatum minima!
                </template>
            </Accordion>
            <Accordion accordion-id="acc-3">
                <template #question>
                    Posso solicitar alterações no design durante o processo?
                </template>
                <template #answer>
                    Lorem, ipsum dolor sit amet consectetur adipisicing elit. Porro inventore repellendus fugit deserunt ipsum sit dolor ab unde nostrum ullam numquam nam illo ex quis accusantium iusto, laudantium voluptatum minima!
                </template>
            </Accordion>
            <Accordion accordion-id="acc-4">
                <template #question>
                    Quanto custa para criar um site?
                </template>
                <template #answer>
                    Lorem, ipsum dolor sit amet consectetur adipisicing elit. Porro inventore repellendus fugit deserunt ipsum sit dolor ab unde nostrum ullam numquam nam illo ex quis accusantium iusto, laudantium voluptatum minima!
                </template>
            </Accordion>
            <Accordion accordion-id="acc-5">
                <template #question>
                    Depois de pronto, preciso pagar alguma mensalidade?
                </template>
                <template #answer>
                    Lorem, ipsum dolor sit amet consectetur adipisicing elit. Porro inventore repellendus fugit deserunt ipsum sit dolor ab unde nostrum ullam numquam nam illo ex quis accusantium iusto, laudantium voluptatum minima!
                </template>
            </Accordion>
            <Accordion accordion-id="acc-6">
                <template #question>
                    Vocês oferecem manutenção ou suporte após a entrega?
                </template>
                <template #answer>
                    Lorem, ipsum dolor sit amet consectetur adipisicing elit. Porro inventore repellendus fugit deserunt ipsum sit dolor ab unde nostrum ullam numquam nam illo ex quis accusantium iusto, laudantium voluptatum minima!
                </template>
            </Accordion>
            <Accordion accordion-id="acc-7">
                <template #question>
                    Eu preciso fornercer todo o conteúdo ou vocês criam tudo?
                </template>
                <template #answer>
                    Lorem, ipsum dolor sit amet consectetur adipisicing elit. Porro inventore repellendus fugit deserunt ipsum sit dolor ab unde nostrum ullam numquam nam illo ex quis accusantium iusto, laudantium voluptatum minima!
                </template>
            </Accordion>
        </div>
    </section>
</template>