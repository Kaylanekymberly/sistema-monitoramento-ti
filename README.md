# Sistema de Monitoramento e Automação de Relatórios de TI

Sistema completo de automação para coleta de métricas de infraestrutura, geração de relatórios e visualização em tempo real através de dashboard web interativo.

![Status](https://img.shields.io/badge/status-active-success.svg)
![Python](https://img.shields.io/badge/python-3.8+-blue.svg)
![License](https://img.shields.io/badge/license-MIT-blue.svg)

##  Sobre o Projeto

Este projeto foi desenvolvido para automatizar o processo de monitoramento de infraestrutura de TI, reduzindo o tempo de geração de relatórios de horas para minutos. O sistema coleta métricas críticas, analisa logs de segurança e gera relatórios profissionais automaticamente.

**Problema resolvido:** Equipes de TI gastam tempo excessivo coletando métricas manualmente e criando relatórios. Este sistema automatiza todo o processo.

##  Funcionalidades

- **Monitoramento em tempo real**
  - CPU, memória RAM e armazenamento
  - Tempo de atividade do sistema
  - Atualização automática a cada 30 segundos

- **Análise histórica**
  - Gráficos de tendência das últimas 24 horas
  - Comparação de métricas ao longo do tempo
  - Visualização de status de backups semanais

- **Logs de segurança**
  - Registro de eventos críticos
  - Classificação por nível (Info, Warning, Critical)
  - Alertas de tentativas de acesso não autorizado

- **Geração automática de relatórios**
  - Relatórios HTML profissionais
  - Envio automático por email
  - Histórico de métricas em JSON

- **Agendamento automatizado**
  - Execução programada via cron (Linux/Mac)
  - Task Scheduler (Windows)
  - Configuração flexível de horários

##  Tecnologias Utilizadas

### Backend
- **Python 3.8+**
- **psutil** - Coleta de métricas do sistema
- **smtplib** - Envio de emails automatizado
- **JSON** - Armazenamento de histórico

### Frontend
- **HTML5 / CSS3**
- **JavaScript (ES6+)**
- **Chart.js** - Visualização de dados
- **Design responsivo**

##  Instalação

### Requisitos
- Python 3.8 ou superior
- pip (gerenciador de pacotes Python)

### Passo a passo

1. Clone o repositório
```bash
git clone https://github.com/seuusuario/sistema-monitoramento-ti.git
cd sistema-monitoramento-ti
```

2. Instale as dependências
```bash
pip install psutil
```

3. Execute o sistema
```bash
python monitoring_system.py
```

4. Acesse o dashboard
```bash
# Abra o arquivo dashboard.html no navegador
# Ou use um servidor local:
python -m http.server 8000
# Acesse: http://localhost:8000/dashboard.html
```

##  Configuração

### Email (opcional)
Para habilitar envio automático de relatórios por email, edite o arquivo `monitoring_system.py`:

```python
sender_email = "seu-email@gmail.com"
sender_password = "sua-senha-de-app"
```

**Nota:** Para Gmail, gere uma senha de app em [myaccount.google.com/apppasswords](https://myaccount.google.com/apppasswords)

### Agendamento automático

**Linux/Mac (cron):**
```bash
crontab -e
# Adicione a linha para executar diariamente às 8h:
0 8 * * * python3 /caminho/completo/monitoring_system.py
```

**Windows (Task Scheduler):**
1. Abra o Agendador de Tarefas
2. Criar Tarefa Básica
3. Gatilho: Diariamente às 08:00
4. Ação: Iniciar programa
   - Programa: `python.exe`
   - Argumentos: `C:\caminho\monitoring_system.py`

## 📊 Estrutura do Projeto

```
sistema-monitoramento-ti/
├── dashboard.html           # Interface web do dashboard
├── monitoring_system.py     # Script Python de coleta e relatórios
├── relatorios/              # Relatórios gerados (criado automaticamente)
│   ├── relatorio_ti_*.html
│   └── historico_metricas.json
├── README.md
└── LICENSE
```

##  Casos de Uso

1. **Equipes de TI corporativas**
   - Monitoramento contínuo de servidores
   - Relatórios automáticos para gestão
   - Análise de tendências de capacidade

2. **Prestadores de serviços MSP**
   - Relatórios para múltiplos clientes
   - SLA tracking
   - Alertas proativos

3. **Ambientes de desenvolvimento**
   - Monitoramento de servidores de teste
   - Análise de performance
   - Debugging de problemas de infraestrutura

##  Roadmap

### Versão atual (v1.0)
- ✅ Dashboard web responsivo
- ✅ Coleta de métricas básicas
- ✅ Geração de relatórios HTML
- ✅ Logs de segurança

### Próximas versões
- [ ] Integração com Flask para dados em tempo real (v1.1)
- [ ] Autenticação de usuários (v1.2)
- [ ] Banco de dados para histórico estendido (v1.3)
- [ ] Alertas via Telegram/Slack (v1.4)
- [ ] API REST completa (v2.0)
- [ ] Dashboard mobile nativo (v2.1)
- [ ] Machine learning para previsão de falhas (v3.0)

##  Contribuindo

Contribuições são bem-vindas! Sinta-se à vontade para:

1. Fazer fork do projeto
2. Criar uma branch para sua feature (`git checkout -b feature/NovaFuncionalidade`)
3. Commit suas mudanças (`git commit -m 'Adiciona nova funcionalidade'`)
4. Push para a branch (`git push origin feature/NovaFuncionalidade`)
5. Abrir um Pull Request

##  Licença

Este projeto está sob a licença MIT. Veja o arquivo [LICENSE](LICENSE) para mais detalhes.

## 👤 Autor

**Kaylane Kimberly**

- LinkedIn:https://www.linkedin.com/feed/
- GitHub:https://github.com/Kaylanekymberly
- Email: kaylanekymberly123@gmai.com

## 🙏 Agradecimentos

Projeto desenvolvido como parte do portfólio acadêmico em Gestão de TI, aplicando conceitos de:
- ITIL (Information Technology Infrastructure Library)
- Governança de TI
- Automação de processos
- DevOps

---

⭐ Se este projeto foi útil para você, considere dar uma estrela no repositório!
