<p align="center"><img src="https://flarum.org/assets/img/logo.png"></p>

<p align="center">
<a href="https://packagist.org/packages/flarum/core"><img src="https://poser.pugx.org/flarum/core/d/total.svg" alt="Total Downloads"></a>
<a href="https://packagist.org/packages/flarum/core"><img src="https://poser.pugx.org/flarum/core/v/stable.svg" alt="Latest Stable Version"></a>
<a href="https://packagist.org/packages/flarum/core"><img src="https://poser.pugx.org/flarum/core/license.svg" alt="License"></a>
</p>

## About Flarum

**[Flarum](https://flarum.org/) is a delightfully simple discussion platform for your website.** It's fast and easy to use, with all the features you need to run a successful community. It is designed to be:

* **Fast and simple.** No clutter, no bloat, no complex dependencies. Flarum is built with PHP so it’s quick and easy to deploy. The interface is powered by Mithril, a performant JavaScript framework with a tiny footprint.

* **Beautiful and responsive.** This is forum software for humans. Flarum is carefully designed to be consistent and intuitive across platforms, out-of-the-box.

* **Powerful and extensible.** Customize, extend, and integrate Flarum to suit your community. Flarum’s architecture is amazingly flexible, with a powerful Extension API.

![screenshot](https://flarum.org/assets/img/home-screenshot.png)

## Installation

Read the **[Installation guide](https://docs.flarum.org/install)** to get started. For support, refer to the [documentation](https://docs.flarum.org/), and ask questions on the [community forum](https://discuss.flarum.org/) or [Discord chat](https://flarum.org/discord/).

## Instalação local, host compartilhado etc...

## 1
composer create project flarum/flarum pasta-do-projeto
## 2
certifique~se de criar um banco de dados para o seu projeto ( estamos partindo de um ponto onde você tem PHP e Mysql instalado) xampp, lampp etc...
## 3
abra um terminal na pasta "public" e digite: php -S localhost:8000
## 4 siga a instalação
acerte o banco de dados admin e etc...
## 5
Se você está localmente tudo deve estar em perfeita ordem, se vai para um host apenas faça o upload dos aquivos e conecte com seu banco de dados por lá
e adcione um arquivo .htaccess com a seguinte diretiva:

<IfModule mod_rewrite.c>
    RewriteEngine On



    RewriteCond %{HTTPS} off
    RewriteRule ^(.*)$ https://%{HTTP_HOST}%{REQUEST_URI} [L,R=301]

    RewriteCond %{REQUEST_URI} !^/public/
    RewriteRule ^(.*)$ /public/$1 [L,QSA]
</IfModule>

Se não estiver com https em seu site visite: https://ssl.startzz.digital e resolva isso.

## Contributing

Thank you for considering contributing to Flarum! Please read the **[Contributing guide](https://docs.flarum.org/contributing)** to learn how you can help.

This repository only holds the Flarum skeleton application. Most development happens in [flarum/core](https://github.com/flarum/core).

## Security Vulnerabilities

If you discover a security vulnerability within Flarum, please follow our [security policy](https://github.com/flarum/core/security/policy) so we can address it promptly.

## License

Flarum is open-source software licensed under the [MIT License](https://github.com/flarum/flarum/blob/master/LICENSE).

