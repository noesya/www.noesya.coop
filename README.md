# www.noesya.coop

[![Netlify Status](https://api.netlify.com/api/v1/badges/25ff53c5-40bd-4c56-9405-a7c16a4aac4e/deploy-status)](https://app.netlify.com/sites/noesya/deploys)

## Setup des domaines

Dans Netlify, domaine principal (avec/sans www) et domaines secondaires (sans www)
- `noesya.netlify.app` (par défaut)
- `www.noesya.coop` (principal)
- `noesya.coop` (redirige vers principal)
- `noesya.com` (alias)
- `noesya.fr` (alias)

Table de redirections dans le fichier [`netlify.toml`](https://github.com/noesya/noesya-www/blob/master/netlify.toml)

### noesya.coop

```
@ 300 IN A 75.2.60.5
www 300 IN CNAME noesya.netlify.app.
```

### noesya.com

*Redirection Web : `http(s)://www.noesya.com` vers `https://www.noesya.coop`*

```
@ 300 IN A 75.2.60.5
www	CNAME	10800	webredir.gandi.net.
```

### noesya.fr

*Redirection Web : `http(s)://www.noesya.fr` vers `https://www.noesya.coop`*

```
@ 300 IN A 75.2.60.5
www	CNAME	10800	webredir.gandi.net.
```
