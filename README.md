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

