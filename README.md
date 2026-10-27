# Claude Desktop File Connector

Yeh ek custom MCP (Model Context Protocol) server hai jo Claude Desktop ko aapke local computer ki files securely access karne deta hai.

## ✨ Features
- **Token Optimization:** `project_map`, `outline_file`, aur `read_symbol` ke zariye poori file parhne ke bajaye sirf zaroori hissa parhta hai.
- **Safety First (Read-Only by Default):** Default mein koi file write/edit nahi hoti. Jab tak aap `config.json` mein `allowWrites: true` na karein.
- **Native Popup Approval:** Write/Edit karte waqt Windows par asli popup (Yes/No) aata hai.
- **Security:** `.env`, `id_rsa` jaisi secret files block hain. UNC, ADS, aur symlinks se bacha jata hai.
- **Deduplication:** Ek dafa parhi hui file ko dobara nahi parhta (agar woh change na hui ho).

## 🚀 Setup Instructions
1. Is repository ko clone karein ya ZIP download karein.
2. Terminal mein is folder mein jayen aur command chalayein:
   ```bash
   npm install