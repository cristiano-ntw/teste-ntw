
# CBR - Colégio Brasileiro de Radiologia

**Product Owner:**  Adáidson

**Dados de Acesso:** [Link](https://docs.google.com/document/d/1iO_9wa-IF008keovOZJpaGvu3ag-jbYQOS2VhWwvf0w/edit#)

**Plano:** Premium

----
| Status | Ambiente | Branch | URL |
|-|-|-|-|
| ![ Wordpress CI/CD ](https://github.com/Apiki/cbr.org.br/workflows/WordPress%20CI/CD/badge.svg?branch=apikihomolog) ![ Theme CI/CD ](https://github.com/Apiki/cbr.org.br/workflows/Theme%20CI/CD/badge.svg?branch=apikihomolog) | Apiki Homolog | apikihomolog | https://cbr.apikihomolog.com |
| ![ Wordpress CI/CD ](https://github.com/Apiki/cbr.org.br/workflows/WordPress%20CI/CD/badge.svg?branch=homolog) ![ Theme CI/CD ](https://github.com/Apiki/cbr.org.br/workflows/Theme%20CI/CD/badge.svg?branch=homolog) | Homolog | homolog | https://homolog.cbr.org.br |
| ![ Wordpress CI/CD ](https://github.com/Apiki/cbr.org.br/workflows/WordPress%20CI/CD/badge.svg?branch=master) ![ Theme CI/CD ](https://github.com/Apiki/cbr.org.br/workflows/Theme%20CI/CD/badge.svg?branch=master) | Produção | master | https://colegiocbr.com.br https://associadocbr.com.br/ |


# WordPress com composer

## Resumo

- Todos os arquivos do WordPress ficaram ignorados
- Plugins e Temas públicos ficaram ignorados
- Plugins e Temas pagos por enquanto ficaram dentro do git
- O tema e os plugins onde o time trabalha ficara dentro do git

## Utilizando o composer para adicionar novos plugins, tema ou atualizar o wordpress.

1. Adicionar o WordPress, plugins e temas no composer, para isso use o [wpackagist](https://wpackagist.org/).

```json
{
  "require": {
    "roots/wordpress": "*",
    "wpackagist-plugin/wordpress-seo": "12.9.1"
  },
  "repositories": [
    {
      "type": "composer",
      "url": "https://wpackagist.org"
    }
  ]
}
```

2. Adicionar no .gitignore o tema usado pelo o time.

```ini
# npm e composer
wp-content/themes/{Nome do Tema}/vendor/ # <-  para ingorar a vendor do tema
wp-content/themes/{Nome do Tema}/dist/ # <- para ignorar a dist do tema

# files to keep
!.gitignore
!.gitlab-ci.yml
!README.md
!composer.json
!composer.lock
!wp-content/themes/{Nome do Tema} # <- para não ignorar o tema
```

## Instale o Wordpress e plugins com o composer

```
 composer install
```

---

# Documentação, guias e padrões

https://docs.apikihomolog.com/

Aqui você irá encontrar guias, documentações e arquivos. Seja bem-vindo!

Você pode contribuir
1. Fork it!
2. Create your feature branch: git checkout -b my-new-feature
3. Commit your changes: git commit -m 'Add some feature'
4. Push to the branch: git push origin my-new-feature
5. Submit a pull request :D