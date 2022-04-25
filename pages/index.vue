<template>
           <div class="center">
            
             
                <ShareNetwork
                  v-for="network in networks"
                  :network="network.network"
                  :key="network.network"
                  title="post.title"
                  description="post.description"
                  class="social-share"
                   :url="sharing.url"
                >
                  <i :class="network.icon"></i>
                  <span>{{ network.name }}</span>
                </ShareNetwork>
          </div>
</template>

<script>
export default {
   data() {

    return {
    	   	 sharing: {
        url: 'https://github.com',
      },

      networks: [
        {
          network: 'facebook',
          name: 'Facebook',
          icon: 'fab fah fa-lg fa-facebook-f',
          color: '#1877f2',
        },
        {
          network: 'pinterest',
          name: 'Pinterest',
          icon: 'fab fah fa-lg fa-pinterest',
          color: '#bd081c',
        },
        {
          network: 'telegram',
          name: 'Telegram',
          icon: 'fab fah fa-lg fa-telegram-plane',
          color: '#0088cc',
        },
        {
          network: 'tumblr',
          name: 'Tumblr',
          icon: 'fab fah fa-lg fa-tumblr',
          color: '#35465c',
        },
        {
          network: 'twitter',
          name: 'Twitter',
          icon: 'fab fah fa-lg fa-twitter',
          color: '#1da1f2',
        },
        {
          network: 'whatsapp',
          name: 'Whatsapp',
          icon: 'fab fah fa-lg fa-whatsapp',
          color: '#25d366',
        },
      ],
    }
  },

    head() {
    return {
      title: 'Social Share',
        meta: [
      { charset: 'utf-8' },
      { name: 'viewport', content: 'width=device-width, initial-scale=1' },
      {
        hid: 'description',
        name: 'description',
        content: 'Social share description',
      },
      { 'http-equiv': 'http-equiv', content: 'text/html; charset=UTF-8' },
    ],
    }
  },
}
</script>
