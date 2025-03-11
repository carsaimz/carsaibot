# 📱 CarsaiBot - Documentação

## 📋 Índice
1. [Introdução](#introdução)
2. [Instalação](#instalação)
3. [Configuração](#configuração)
4. [Comandos](#comandos)
5. [Sistemas](#sistemas)
6. [API](#api)
7. [Administração](#administração)
8. [Solução de Problemas](#solução-de-problemas)
9. [FAQ](#faq)

## 📌 Introdução

CarsaiBot é um bot WhatsApp completo desenvolvido com Baileys, oferecendo múltiplos sistemas e funcionalidades.

### Características Principais
- Sistema de economia virtual
- Jogos e diversão
- Downloads de mídia
- Gerenciamento de grupos
- Painel web administrativo
- Sistema de backup automático

## 💻 Instalação

### Requisitos do Sistema
- Node.js 18+
- FFmpeg
- Python 3
- 2GB RAM (mínimo)
- 20GB Espaço em disco

### Passo a Passo

1. Instale as dependências:
```bash
./install_dependencies.sh
```

2. Instale o bot:
```bash
./install.sh
```

3. Inicie o bot:
```bash
# Opção 1 - Modo normal
./start.sh

# Opção 2 - Modo desenvolvimento
./dev.sh

# Opção 3 - Com PM2
pm2 start ecosystem.config.js
```

## ⚙️ Configuração

### Arquivo config.json
```json
{
    "name": "NomeDoBot",
    "prefix": "!",
    "owner": ["258862414345@s.whatsapp.net"],
    "supportGroup": "https://chat.whatsapp.com/HgYs7Rk3T9sGdrJxGRQzri",
    "language": "pt-BR",
    "antiSpam": true,
    "antiLink": true
}
```

### Configurações Disponíveis
| Configuração | Descrição | Padrão |
|-------------|-----------|---------|
| name | Nome do bot | CarsaiBot |
| prefix | Prefixo dos comandos | ! |
| antiSpam | Anti-spam | true |
| antiLink | Anti-link | true |
| maxWarnings | Máximo de advertências | 3 |

## 🎮 Comandos

### Economia
| Comando | Descrição | Uso |
|---------|-----------|-----|
| !daily | Recebe bônus diário | !daily |
| !pay | Transfere dinheiro | !pay @user 1000 |
| !balance | Ver saldo | !balance |

### Diversão
| Comando | Descrição | Uso |
|---------|-----------|-----|
| !tictactoe | Jogo da velha | !tictactoe @user |
| !hangman | Jogo da forca | !hangman |
| !dice | Rolar dados | !dice 6 |

### Downloads
| Comando | Descrição | Uso |
|---------|-----------|-----|
| !play | Baixa música | !play nome da música |
| !video | Baixa vídeo | !video URL |
| !tiktok | Baixa TikTok | !tiktok URL |

### Administração
| Comando | Descrição | Uso |
|---------|-----------|-----|
| !ban | Bane usuário | !ban @user |
| !warn | Adverte usuário | !warn @user motivo |
| !settings | Configurações | !settings list |

## 🔧 Sistemas

### Sistema de Economia
- Moeda virtual
- Transferências
- Loja virtual
- Ranking

### Sistema de Jogos
- Jogo da velha
- Forca
- Dados
- Ranking global

### Sistema de Downloads
- YouTube (áudio/vídeo)
- TikTok
- Instagram
- Gerenciamento automático

### Sistema de Grupos
- Anti-link
- Anti-spam
- Bem-vindo
- Advertências

## 🌐 API

### Endpoints
```javascript
GET /api/stats - Estatísticas do bot
POST /api/message - Envia mensagem
GET /api/logs - Logs do sistema
```

### WebSocket
```javascript
socket.on('stats', (data) => {
    // Recebe estatísticas em tempo real
});
```

## 👑 Administração

### Painel Web
- URL: http://seu-ip:3000
- Login: admin
- Senha: definida na instalação

### Recursos
- Monitoramento em tempo real
- Gerenciamento de usuários
- Logs do sistema
- Backup/Restore

## ❗ Solução de Problemas

### Erros Comuns

1. Bot não conecta
```bash
# Verifique os logs
pm2 logs carsaibot

# Limpe a sessão
rm -rf auth_info_baileys
```

2. Comandos não funcionam
```bash
# Verifique as permissões
ls -l plugins/

# Recarregue os comandos
!reload
```

3. Erros de memória
```bash
# Aumente o limite de memória
NODE_OPTIONS="--max-old-space-size=4096"
```

## ❓ FAQ

### Perguntas Frequentes

1. Como adicionar novos comandos?
- Crie um arquivo .js na pasta plugins/
- Use o modelo de comando existente
- Reinicie o bot

2. Como fazer backup?
```bash
# Backup manual
!backup

# Backup automático
Configurado para rodar a cada 24h
```

3. Como atualizar o bot?
```bash
# Atualize os arquivos
git pull

# Atualize as dependências
npm install

# Reinicie o bot
pm2 restart carsaibot
```

### Dicas e Truques

1. Performance
- Use PM2 para gerenciamento
- Ative o modo de baixo consumo
- Configure limites de uso

2. Segurança
- Mantenha o config.json seguro
- Use senhas fortes
- Faça backups regulares

3. Customização
- Edite as mensagens em src/messages/
- Personalize o menu em plugins/menu.js
- Adicione seus próprios comandos

## 📞 Suporte

- Grupo: [https://chat.whatsapp.com/HgYs7Rk3T9sGdrJxGRQzri](https://chat.whatsapp.com/HgYs7Rk3T9sGdrJxGRQzri)
- Issues: GitHub Issues
- Email: [carsaimozambique@gmail.com](carsaimozambique@gmail.com)

## 📝 Licença

Este projeto está sob a licença MIT. Veja o arquivo [LICENSE](LICENSE) para mais detalhes.

---
**Nota**: Mantenha esta documentação atualizada conforme o bot evolui.# carsaibot
# carsaibot
# carsaibot
# carsaibot
