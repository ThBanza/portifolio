<template>
    <div class="content-vh">
        <div class="content">
            <a-typography-title style="font-weight: bold; font-size: 40px;">
                Vamos entrar em contato:
                <span style="color: #1677FF;">maneiras de se conectar comigo</span>
            </a-typography-title>
            <a-typography-paragraph>
                Obrigado pelo seu interesse em entrar em contato comigo. Agradeço seus comentários, perguntas e sugestões. Se você tiver uma pergunta ou comentário específico, 
                sinta-se à vontade para me enviar um e-mail diretamente para <span style="color: #1677FF">{{ content.email }}</span> Faço um esforço para responder a todas as mensagens dentro de 24 horas, embora possa demorar mais em períodos de maior movimento . 
                Finalmente, se preferir se conectar nas redes sociais, você pode se conectar comigo usando os links de redes sociais abaixo.
            </a-typography-paragraph>

            <a :href="content.social_links.facebook" target="_blank">
                <a-button type="text">
                    <facebook-outlined /> Siga-me no Facebook
                </a-button>
            </a>

            <br />

            <a :href="content.social_links.instagram" target="_blank">
                <a-button type="text">
                    <instagram-outlined /> Siga-me no Instagram
                </a-button>
            </a>

            <br />

            <a :href="content.social_links.twitter" target="_blank">
                <a-button type="text">
                    <twitter-outlined /> Siga-me no Twitter
                </a-button>
            </a>

            <br />

            <a :href="content.social_links.linkedin" target="_blank">
                <a-button type="text">
                    <linkedin-outlined /> Siga-me no Linkedin
                </a-button>
            </a>

            <a-divider></a-divider>

            <a :href="'mailto:' + content.email">
                <a-button type="text">
                    <mail-outlined /> thomazbanza@gmail.com
                </a-button>
            </a>
        </div>
    </div>
</template>

<script setup lang="ts">
import content from '~/static/content.json';

useHead({
    title: "Contact",
})
</script>

<style scoped>
.ant-typography {
    font-size: 16px;
}

.ant-btn {
    font-size: 16px;
}

.anticon {
    color: #1677FF;
}

.content {
    width: 100%;
}

/* lg */
@media (min-width: 1024px) {
    .content {
        width: 80%;
    }
}
</style>