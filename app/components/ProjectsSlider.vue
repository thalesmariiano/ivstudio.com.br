<template>
    <div class="w-full py-16 bg-gradient-to-t from-black from-70%">
        <div class="w-full max-w-4xl flex justify-between items-center mx-auto mb-10">
            <p class="font-poppins font-medium text-white italic">
                <span class="text-neutral-500">//</span>
                Confira alguns projetos
            </p>
            <a class="flex gap-2 items-center text-white font-poppins font-light italic">
                Veja mais projetos
                <IconsArrowForward width="18" height="18" stroke="#fff" />
            </a>
        </div>
        <div class="w-full flex gap-5 justify-center items-center">
            <ProjectCard />
            <ProjectCard />
            <ProjectCard />
            <ProjectCard />
            <ProjectCard />
        </div>
    </div>
</template>