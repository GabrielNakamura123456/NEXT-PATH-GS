# 🚀 NEXT PATH – DevOps Infrastructure  
### Global Solution – DevOps Tools & Cloud Computing  
### FIAP – Engenharia de Software – 2025  

Este repositório contém toda a infraestrutura em nuvem criada na AWS EC2 para o projeto **NEXT PATH**, uma solução integrada para requalificação profissional e gestão de trilhas de aprendizado, alinhada ao tema SkillUp AI.

A entrega inclui:

- Provisionamento das VMs (Windows + Linux)
- Instalação do MySQL Server
- Configuração de usuário e privilégios
- CRUD completo realizado no banco
- Instalação do Docker Engine
- Testes de containers
- Prints das evidências
- Documentação exigida pela GS

---

## 📌 1. Objetivo do Projeto (NEXT PATH)

O **NEXT PATH** é o ambiente técnico da plataforma educacional que auxiliará usuários no desenvolvimento profissional, com APIs, dashboards e integrações com IA.

O objetivo da GS é demonstrar competências de *Cloud Computing + DevOps*, criando:

- 1 VM Windows (painel administrativo)
- 1 VM Linux (backend + banco)
- MySQL configurado com acesso remoto
- Docker instalado e funcional
- CRUD comprovado em vídeo
- Segurança via Security Groups
- Documentação em PDF + GitHub

---

## 📌 2. Arquitetura do Projeto

### 🟦 VM Windows – EC2
- Windows Server 2025 Datacenter  
- Porta: 3389 (RDP)  
- Utilização: administração e validações

---

### 🟩 VM Linux – EC2 (Ubuntu)
- Ubuntu Server 24.04 LTS  
- Portas abertas:  
  - 22 (SSH)  
  - 3306 (MySQL)  
- Ferramentas instaladas:  
  - MySQL Server  
  - Docker Engine  
  - Docker Compose Plugin  

---

### 🟧 Banco de Dados – MySQL
- Banco: `nextpath_db`  
- Usuário: `nextpath_user`  
- Permissões completas  
- CRUD validado durante a GS  

---

## 📌 3. Prints de Evidência

As imagens estão na pasta:

Incluindo:

- Criação das VMs  
- Conexão SSH  
- MySQL funcionando  
- CRUD completo  
- Docker rodando  

---

## 📌 4. Instalação – Ubuntu

```bash
sudo apt update -y
sudo apt upgrade -y
5. MySQL – Instalação
sudo apt install mysql-server -y
sudo mysql_secure_installation

📌 6. MySQL – Configuração

Entrar no MySQL:

sudo mysql -u root


Criar banco:

CREATE DATABASE nextpath_db;


Criar usuário:

CREATE USER 'nextpath_user'@'%' IDENTIFIED BY 'SenhaForte123!';


Permissões:

GRANT ALL PRIVILEGES ON *.* TO 'nextpath_user'@'%' WITH GRANT OPTION;
FLUSH PRIVILEGES;

📌 7. CRUD – Banco Next Path
INSERT INTO alunos (nome, idade) VALUES ('Gabriel', 22);
SELECT * FROM alunos;
UPDATE alunos SET idade = 23 WHERE nome = 'Gabriel';
DELETE FROM alunos WHERE nome = 'Gabriel';

📌 8. Docker
sudo apt install ca-certificates curl gnupg -y
sudo apt install docker-ce docker-ce-cli containerd.io docker-buildx-plugin docker-compose-plugin -y
sudo usermod -aG docker $USER
docker run hello-world

📌 9. Conclusão

Infraestrutura NEXT PATH implantada com sucesso:

VMs funcionando

Banco configurado

CRUD concluído

Docker ativo

Segurança aplicada

Documentação entregue

Pronto para integração com as demais disciplinas (Java, .NET, Mobile, IoT, TOGAF).
