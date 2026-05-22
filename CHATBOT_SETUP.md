# Lab Assistant setup

The `Ask` button works immediately with a local helper. To enable the real AI chatbot, deploy the Supabase Edge Function in this folder.

## 1. Install tools

Install Git and the Supabase CLI on the computer you use for publishing.

## 2. Link Supabase

From the `06` folder:

```bash
supabase login
supabase link --project-ref mvirpcwcclneaanxtjpr
```

## 3. Add your OpenAI key as a Supabase secret

```bash
supabase secrets set OPENAI_API_KEY=your_openai_api_key_here
```

Do not paste the OpenAI key into `index.html`.

## 4. Deploy the function

```bash
supabase functions deploy lab-assistant
```

## 5. Publish the web app

Copy the updated `index.html`, `manifest.json`, `sw.js`, and `icon.svg` to the GitHub repository that publishes:

```text
https://castlecraig-cyber.github.io/lab-tools/
```

After GitHub Pages refreshes, open the site, sign in, and press `Ask`.
