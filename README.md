# Broken tsconfig.json passes using `vercel dev`


```
❯ vercel dev   
Vercel CLI 22.0.1 dev (beta) — https://vercel.com/feedback
> Ready! Available at http://localhost:3000

```

browse http://localhost:3000/api/hello?name=vercel 

# fails using `vercel`

```
❯ vercel    
Vercel CLI 22.0.1
🔍  Inspect: https://vercel.com/ramondonnell/vercel-93848/FwCRQ4qFbPzy6DtuFhnWdBMfqYnU [3s]
Error! tsconfig.json(10,12): error TS1002: Unterminated string literal.

Error! Check your logs at https://vercel-93848-o4z764cjh-ramondonnell.vercel.app/_logs or run `vercel logs vercel-93848-o4z764cjh-ramondonnell.vercel.app`


```

# fails on [vercel dashboard](https://vercel.com/ramondonnell/vercel-93848/2V3JWh8ZRij4o2kyYeMksocJdjwi) after push

```
07:24:27.584  	Cloning github.com/RamonDonnell/vercel-93848 (Branch: master, Commit: be1cf00)
07:24:28.086  	Cloning completed in 502ms
07:24:28.093  	Analyzing source code...
07:24:28.483  	Installing build runtime...
07:24:29.093  	Build runtime installed: 609.340ms
07:24:30.705  	Looking up build cache...
07:24:30.812  	Build cache not found
07:24:31.596  	Installing dependencies...
07:24:32.056  	npm WARN read-shrinkwrap This version of npm is compatible with lockfileVersion@1, but package-lock.json was generated for lockfileVersion@2. I'll try to do my best with it!
07:24:33.051  	npm WARN workpath0 No description
07:24:33.059  	npm WARN workpath0 No repository field.
07:24:33.068  	npm WARN workpath0 No license field.
07:24:33.070  	added 11 packages from 83 contributors in 1.037s
07:24:33.278  	Using TypeScript 3.9.3 (local user-provided)
07:24:33.291  	tsconfig.json(10,12): error TS1002: Unterminated string literal.
07:24:34.699  	Uploading build outputs...
07:24:35.098  	Deploying build outputs...
07:24:35.775  	Done with static build
07:24:37.823  	Done with "api/hello.ts"
```

