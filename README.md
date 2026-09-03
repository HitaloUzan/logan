# Site Logan Serviços de Tecnologia

Site institucional estático (um único arquivo `index.html`, sem build, sem backend).

## Estrutura

```
/
└── index.html
```

Só isso. É importante que `index.html` fique na **raiz** do repositório (não dentro de `/public`, `/src` etc.), senão o Vercel/GitHub Pages não encontra o arquivo e mostra 404.

## Deploy no GitHub

1. No repositório `HitaloUzan/logan`, apague qualquer arquivo antigo com outro nome (ex: `logan-site.html`) e suba este `index.html` na raiz.
2. Commit direto na branch `main`.

## Deploy no Vercel

1. Em **New Project**, importe o repositório `HitaloUzan/logan`.
2. Em **Application Preset**, troque de "FastHTML" para **Other** (site estático puro, sem framework).
3. **Root Directory**: deixe `./`.
4. **Build and Output Settings**: pode deixar em branco/padrão — não há build.
5. Clique em **Deploy**.

Se o projeto já existir com o preset errado, vá em **Settings → General → Framework Preset**, troque para "Other" e depois em **Deployments → Redeploy**.

## Domínio próprio

Depois do deploy funcionar em `algumacoisa.vercel.app`:

1. Compre o domínio (Registro.br para `.com.br`, ou qualquer registrador para outros).
2. No projeto Vercel, vá em **Settings → Domains** e adicione o domínio.
3. A Vercel mostra os registros DNS (geralmente um `A` ou `CNAME`) para configurar no painel do seu registrador.
4. Propagação de DNS pode levar de minutos a algumas horas.
