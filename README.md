# cf-vue

#### buat project baru
1. pastikan sudah install nodejs dan GIT.
2. buka terminal dan pilih folder tempat project.
3. jalankan `npm create vue@latest`.
4. Project name isi dengan `cf-vue`.
5. untuk feature pilih `Router` saja.

##### menjalankan project
1. buka folder `cf-vue` di vscode.
2. buka terminal yang ada di vscode dengan ctrl + `.
3. install dependency project dengan menjalankan `npm install` di terminal.
4. jalankan project dengan menjalankan `npm run dev` di terminal.

#### setting github
1. menu source control di vscode pilih `Initialize Repository`.
2. tambah readme dan commit dengan pesan `init`.
3. buat blank repository di github, dengan nama `cf-vue`, pilih public, klik `create repository`.
4. menu (...) samping changes pilih `remote` -> `add remote` -> `add remote from github` -> beri nama origin.
5. publish/push ke github.

#### koneksi ke cloudflare.
1. buka terminal dan tambahkan cf dependency dengan `npm i -D @cloudflare/vite-plugin wrangler`.
2. setting `vite.config.js` dan `wrangler.jsonc`.
3. login cloudflare, pilih menu `compute (worker)`, create `workers`, pilih dari `import repository`, pilih project `cf-vue`.
4. setting default lalu pilih `save and deploy`.

#### setting backend dan db
1. install hono dengan menjalankan `npm install hono` di terminal.
2. setting file `api/index.js` menggunakan hono.
3. buat database dengan nama `cf-vue` di cloudflare kemudian ambil id nya.
4. pada `wrangler.json` setting `assets`, `d1_databases` dan `main`.
5. buat migrasi dengan menjalankan `npx wrangler d1 migrations create cf-vue create_users`.
6. setting file `0001_create_users.sql`.
7. jalankan migrasi dengan `npx wrangler d1 migrations apply cf-vue`.
8. untuk menjalankan migrasi di serve tambahkan flag `--remote`: `npx wrangler d1 migrations apply cf-vue --remote`
9. setting api pada route `/api/users`.
