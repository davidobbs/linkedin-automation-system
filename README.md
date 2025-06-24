# 🤖 LinkedIn Inbox Automation System

Sistema completo de automação para monitoramento e resposta automática do inbox do LinkedIn com arquitetura híbrida JavaScript/Python.

## 🎯 Visão Geral

Este sistema permite automatizar completamente o processo de monitoramento e resposta de mensagens no LinkedIn, mantendo um comportamento natural e evitando detecção. Ideal para profissionais que recebem muitas mensagens e querem manter um alto nível de engajamento.

### ✨ Principais Funcionalidades

- **🔍 Monitoramento Inteligente**: Verifica periodicamente novas mensagens no inbox
- **🧠 Análise Automática**: Classifica mensagens por tipo e sentimento
- **💬 Respostas Contextuais**: Gera respostas personalizadas baseadas no contexto
- **🛡️ Sistema Anti-Detecção**: Simula comportamento humano natural
- **📊 Relatórios Detalhados**: Analytics completos de engajamento
- **🤖 Integração com IA**: Suporte para OpenAI e Anthropic

## 🚀 Instalação Rápida

```bash
# Clone o repositório
git clone https://github.com/davidobbs/linkedin-automation-system.git
cd linkedin-automation-system

# Execute o setup automático
chmod +x scripts/setup.sh
./scripts/setup.sh

# Configure suas variáveis de ambiente
cp .env.example .env
# Edite o arquivo .env com suas configurações

# Inicie o sistema
./scripts/start.sh
```

## 📋 Pré-requisitos

- **Node.js** 16+ 
- **Python** 3.8+
- **Chrome/Chromium** browser
- **Conta LinkedIn** ativa

## 🎮 Como Usar

### Modo Rápido
```bash
# Inicia interface de seleção
./scripts/start.sh
```

### Modo JavaScript (Desenvolvimento)
```bash
npm start
```

### Modo Python (Produção)
```bash
python3 python/inbox_automation.py
```

### Executar Testes
```bash
npm test
```

## ⚙️ Configuração

### Arquivo Principal: `config/inbox_config.json`

```json
{
  "monitoring": {
    "check_interval": 300,
    "max_messages_per_check": 10,
    "enable_ai_responses": false
  },
  "anti_detection": {
    "random_delays": true,
    "human_typing_simulation": true
  }
}
```

### Templates de Resposta: `templates/response_templates.json`

Personalize as respostas automáticas por categoria:
- Lead interessado
- Pergunta geral  
- Objeção
- Agradecimento
- Networking
- Follow-up

### Variáveis de Ambiente: `.env`

```env
# IA (Opcional)
OPENAI_API_KEY=your_key_here
ANTHROPIC_API_KEY=your_key_here

# Notificações (Opcional)
SMTP_SERVER=smtp.gmail.com
EMAIL_USER=your_email@gmail.com
```

## 🏗️ Arquitetura

```
linkedin-automation-system/
├── src/
│   ├── modules/
│   │   └── inbox-monitor.js      # Módulo principal JavaScript
│   └── index.js                  # Entry point JavaScript
├── python/
│   └── inbox_automation.py       # Sistema Python completo
├── templates/
│   └── response_templates.json   # Templates de resposta
├── config/
│   └── inbox_config.json         # Configurações principais
├── scripts/
│   ├── setup.sh                  # Script de instalação
│   └── start.sh                  # Script de inicialização
├── tests/
│   └── test-inbox-monitor.js     # Testes automatizados
├── logs/                         # Logs do sistema
└── docs/                         # Documentação completa
```

## 🔧 Funcionalidades Avançadas

### Sistema Anti-Detecção
- Delays aleatórios entre ações
- Simulação de digitação humana
- Movimentos naturais do mouse
- Intervalos de descanso programados

### Classificação Inteligente
- **Lead Interessado**: Detecta interesse comercial
- **Pergunta Geral**: Identifica dúvidas e questionamentos
- **Objeção**: Reconhece resistências e preocupações
- **Agradecimento**: Identifica mensagens de gratidão
- **Networking**: Detecta tentativas de conexão profissional

### Personalização Avançada
- Respostas contextuais por horário
- Personalização por empresa e cargo
- Histórico de conversas
- Análise de sentimento

## 📊 Relatórios e Analytics

O sistema gera automaticamente:
- Relatórios diários de atividade
- Estatísticas de engajamento
- Análise de performance
- Métricas de resposta
- Distribuição de tipos de mensagem

## 🛡️ Segurança e Compliance

- Respeita rate limits do LinkedIn
- Simula comportamento humano natural
- Logs detalhados para auditoria
- Configurações de horário de funcionamento
- Sistema de backup automático

## 🔍 Troubleshooting

### Problemas Comuns

**Navegador não abre:**
```bash
# Instala dependências do Chrome
sudo apt-get install -y libxss1 libappindicator1
```

**Erro de login:**
- Use perfil do navegador com login salvo
- Desative 2FA temporariamente
- Configure `user_data_dir` corretamente

**Mensagens não detectadas:**
- Verifique se LinkedIn mudou interface
- Ative modo debug: `DEBUG=true npm start`
- Consulte logs em `logs/`

## 📈 Roadmap

- [ ] Interface web para configuração
- [ ] Suporte a múltiplas contas
- [ ] Integração com CRM
- [ ] Machine Learning para classificação
- [ ] API REST para controle externo
- [ ] Dashboard em tempo real

## 🤝 Contribuição

1. Fork o projeto
2. Crie sua feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit suas mudanças (`git commit -m 'Add AmazingFeature'`)
4. Push para a branch (`git push origin feature/AmazingFeature`)
5. Abra um Pull Request

## 📄 Licença

Este projeto está licenciado sob a MIT License.

## ⚠️ Disclaimer

Este software é fornecido apenas para fins educacionais e de automação pessoal. O uso deve estar em conformidade com os Termos de Serviço do LinkedIn. Os desenvolvedores não se responsabilizam por qualquer uso inadequado.

## 📞 Suporte

- 📖 [Documentação Completa](docs/INBOX_AUTOMATION.md)
- 🐛 [Reportar Bug](https://github.com/davidobbs/linkedin-automation-system/issues)
- 💡 [Solicitar Feature](https://github.com/davidobbs/linkedin-automation-system/issues)
- 📧 Suporte: [Abrir Issue](https://github.com/davidobbs/linkedin-automation-system/issues)

---

**Desenvolvido com ❤️ para automação inteligente do LinkedIn**

### 🎯 Casos de Uso

- **Vendedores**: Resposta automática a leads interessados
- **Recrutadores**: Triagem inicial de candidatos
- **Consultores**: Qualificação de prospects
- **Empreendedores**: Networking automatizado
- **Freelancers**: Gestão de propostas comerciais

### 📱 Compatibilidade

- ✅ Linux (Ubuntu, CentOS, Debian)
- ✅ macOS
- ✅ Windows (WSL recomendado)
- ✅ Docker (em desenvolvimento)
- ✅ Cloud (AWS, GCP, Azure)