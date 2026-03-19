<template>
    <div ref="wrapper">
        <div ref="content">
            <AppHeader />
                <slot />
            <AppFooter />
        </div>
        <FloatingWhatsapp />
    </div>
</template>