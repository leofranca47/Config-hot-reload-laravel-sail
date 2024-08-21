# Config-hot-reload-laravel-sail
Configurações para funcionar o hot reload utilizando o laravel sail

adicionar o server no vite.config.js

~~~php
import { defineConfig } from 'vite';
import laravel from 'laravel-vite-plugin';

export default defineConfig({
    server: {
        hmr: {
            host: 'localhost',
        },
        watch: {
            usePolling: true
        }
    },
    plugins: [
        laravel({
            input: ['resources/css/app.css', 'resources/js/app.js'],
            refresh: true,
        }),
    ],
});
~~~
