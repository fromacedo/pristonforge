<div align="center">
  <img src="https://i.postimg.cc/W4PyGbVV/Priston-Forge-Avatar.jpg" alt="PristonForge Logo" width="140" height="140" style="border-radius: 50%; border: 3px solid #FF4500;">

  # 🛡️ PristonForge

  **O assistente definitivo de Discord para clãs e jogadores de Priston Tale Brasil (BPT).**

  [![Node.js](https://img.shields.io/badge/Node.js-18.x+-339933?style=for-the-badge&logo=nodedotjs&logoColor=white)](https://nodejs.org/)
  [![Discord.js](https://img.shields.io/badge/Discord.js-v14-5865F2?style=for-the-badge&logo=discord&logoColor=white)](https://discord.js.org/)
  [![MongoDB](https://img.shields.io/badge/MongoDB-Atlas-47A248?style=for-the-badge&logo=mongodb&logoColor=white)](https://www.mongodb.com/)
  [![Puppeteer](https://img.shields.io/badge/Puppeteer-Stealth-40B5A4?style=for-the-badge&logo=puppeteer&logoColor=white)](https://pptr.dev/)

  <br>

  [![Adicionar ao Discord](https://img.shields.io/badge/Adicionar_ao_Discord-5865F2?style=for-the-badge&logo=discord&logoColor=white)](https://discord.com/oauth2/authorize?client_id=1493293459514331326&permissions=8&integration_type=0&scope=bot+applications.commands)
</div>

---

## 📖 Sobre o Projeto

O **PristonForge** foi desenvolvido para automatizar a gestão de guildas e auxiliar jogadores de **Priston Tale** diretamente no Discord. Ele combina uma base de dados auditada com a Wiki Oficial do jogo, monitoramento em tempo real dos minutos dinâmicos dos Bosses (Alfa a Zeta) e integração com o ranking oficial da Zenit Games.

Projetado com foco em **alta disponibilidade e segurança (Anti-Ban)**, o bot utiliza cache inteligente e banco de dados em nuvem (MongoDB) para responder instantaneamente aos comandos sem sobrecarregar os servidores oficiais.

---

## ✨ Principais Funcionalidades

* 🎯 **Radar de Bosses ao Vivo:** Monitora os minutos dinâmicos dos sub-servidores (Alfa, Beta, Gama, Delta, Ômega e Zeta) e realiza postagens automáticas diárias no canal oficial do clã.
* ⏰ **Consulta de Boss da Hora:** Cruza a janela de horário atual (fuso horário de Brasília) com a base oficial de Bosses Especiais, exibindo mapa, nível e horários exatos de nascimento.
* 🔔 **Despertador Pessoal (DM):** Sistema de alarme único que envia uma mensagem privada ao jogador exatamente **10 minutos antes** do Boss escolhido nascer.
* 🪪 **Carteira de Aventureiro:** Vinculação de conta que gera um cartão personalizado com Nível, Classe, ícone oficial, Posição no Ranking, Tier, Título e barra de progresso rumo ao Level Cap.
* 🏆 **Hall da Fama do Clã (`Top 10`):** Ranking interno automático que organiza os membros mais fortes registrados no Discord da guilda através de leitura local ultrarrápida.
* 🕵️ **Radar Olheiro Global:** Pesquisa avulsa de qualquer personagem e servidor na base da Zenit sem interferir no perfil vinculado do usuário.
* 🔘 **Botões Interativos:** Atualização rápida de perfil e consulta instantânea do Boss da Hora diretamente pelos botões anexados aos painéis.

---

## 🎮 Lista de Comandos (`Slash Commands`)

### 🪪 Personagem e Ranking
| Comando | Parâmetros | Descrição |
| :--- | :--- | :--- |
| `/registrar` | `nick` `servidor` | Vincula permanentemente o seu personagem principal à sua conta do Discord. |
| `/perfil` | *Nenhum* | Exibe a sua Carteira de Aventureiro com botão de atualização rápida. |
| `/topclan` | *Nenhum* | Mostra o Hall da Fama (Top 10) dos membros registrados no servidor do Discord. |
| `/consultar` | `nick` `servidor` | Consulta a ficha e o ranking de qualquer jogador ou personagem secundário (*alt*). |

### ⚔️ Caçada e Bosses
| Comando | Parâmetros | Descrição |
| :--- | :--- | :--- |
| `/bossatual` | *Nenhum* | Lista todos os Bosses Especiais previstos para nascer na hora atual e seus mapas. |
| `/timeboss` | *Nenhum* | Envia o painel de minutos dinâmicos no canal oficial com botão interativo. |
| `/avisar` | `boss` *(Autocomplete)* | Ativa ou desativa um alarme via DM 10 minutos antes do nascimento do Boss. |

### ⚙️ Administração (Apenas Administradores)
| Comando | Parâmetros | Descrição |
| :--- | :--- | :--- |
| `/config` | `canal` `servidor` `level_cap` | Configura o canal de avisos, o servidor alvo e sincroniza a base de Bosses no MongoDB. |
| `/levelcap` | `cap` | Atualiza rapidamente o limite de nível do servidor para recalibrar as barras de progresso. |
| `/status` | *Nenhum* | Exibe o diagnóstico técnico do bot, servidor vigiado e latência (Ping). |
| `/ajuda` | *Nenhum* | Exibe o manual resumido de comandos dentro do Discord. |

---

## 🛡️ Base Oficial de Bosses Especiais

O núcleo do **PristonForge** conta com uma base blindada e sincronizada com a Wiki Oficial:

| Boss Especial | Nível | Mapa Oficial | Janelas de Horário (Time Boss) |
| :--- | :---: | :--- | :--- |
| **Babel (I1)** | 105 | Estrada de Ferro do Caos | `00:xx, 03:xx, 06:xx, 09:xx, 12:xx, 15:xx, 18:xx, 21:xx` |
| **Babel (I2)** | 105 | Coração de Perum | `01:xx, 04:xx, 07:xx, 10:xx, 13:xx, 16:xx, 19:xx, 22:xx` |
| **Fúria** | 105 | Templo Maldito - 3º Andar | `02:xx, 05:xx, 08:xx, 11:xx, 14:xx, 17:xx, 20:xx, 23:xx` |
| **Valento** | 110 | Vale Gallubia | `01:xx, 05:xx, 09:xx, 13:xx, 17:xx, 21:xx` |
| **Kelvezu** | 115 | Covil do Kelvezu | `01:xx, 07:xx, 13:xx, 19:xx` |
| **Mokova** | 120 | Templo Perdido | `02:xx, 08:xx, 14:xx, 20:xx` |
| **Shy** | 125 | Torre Sem Fim - 3º Andar | `07:xx, 15:xx, 23:xx` |
| **Tulla** | 130 | Mina de Gelo - 1º Andar | `04:xx, 12:xx, 20:xx` |
| **Draxos** | 135 | Laboratório Secreto | `09:xx, 19:xx` |
| **Greedy** | 140 | Arma Antiga | `10:xx, 21:xx` |
| **Espectro do Midranda** | 150 | Estrada Sombria | `11:xx, 19:xx` |
| **Dragão de Snowstorm** | 160 | Abismo do Mar Congelado | `11:xx, 22:xx` |
| **Yagditha** | 160 | Abismo do Mar | `04:xx, 10:xx, 16:xx, 22:xx` |
| **Zuepi** | 55 a 165 | Vários Mapas | `05:xx, 11:xx, 17:xx, 23:xx` |
| **Midranda Ressurgido** | 180 | Santuário do Abismo | `19:xx` |
| **Dama Flamejante** | 190 | Coração de Fogo | `22:xx, 23:xx` |

---

## 🚀 Como Executar o Projeto Localmente

### Pré-requisitos
* [Node.js](https://nodejs.org/) (v18 ou superior)
* Uma conta e cluster no [MongoDB Atlas](https://www.mongodb.com/cloud/atlas)
* Uma aplicação criada no [Discord Developer Portal](https://discord.com/developers/applications)

### Passo a Passo

1. **Clone o repositório:**
   ```bash
   git clone [https://github.com/SEU-USUARIO/pristonforge.git](https://github.com/SEU-USUARIO/pristonforge.git)
   cd pristonforge
   ```

2. **Instale as dependências:**
   ```bash
   npm install discord.js dotenv mongoose puppeteer puppeteer-extra puppeteer-extra-plugin-stealth
   ```

3. **Configure as variáveis de ambiente:**
   Crie um arquivo chamado `.env` na raiz do projeto e preencha com as suas credenciais:
   ```env
   DISCORD_TOKEN=seu_token_do_bot_aqui
   CLIENT_ID=id_da_sua_aplicacao_discord_aqui
   MONGO_URI=sua_string_de_conexao_do_mongodb_aqui
   ```

4. **Inicie o bot:**
   ```bash
   node index.js
   ```

5. **Sincronize no Discord:**
   Assim que o bot ficar online, entre no seu servidor do Discord e execute o comando `/config` para definir o canal de avisos e popular o banco de dados pela primeira vez.

---

## 📂 Estrutura de Arquivos

```text
📦 pristonforge
 ┣ 📜 index.js        # Núcleo do bot, comandos Slash, eventos, botões e conexão MongoDB
 ┣ 📜 scraper.js      # Motor Puppeteer Stealth com fila de requisições e base oficial de Bosses
 ┣ 📜 index.html      # Landing Page e Manual Oficial (Bootstrap 5) para GitHub Pages
 ┣ 📜 package.json    # Gerenciador de dependências do Node.js
 ┣ 📜 .env            # Variáveis sensíveis (não enviar para o GitHub!)
 ┗ 📜 README.md       # Documentação oficial do repositório
```

---

## ⚠️ Aviso de Segurança (`.gitignore`)

Antes de subir os seus arquivos para o GitHub, crie um arquivo `.gitignore` na pasta do projeto para garantir que a sua senha do banco de dados e o token do bot **nunca** fiquem públicos:

```text
node_modules/
.env
```

---

<div align="center">
  Desenvolvido com 🔥 por <strong>PristonForge</strong>
</div>