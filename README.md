# 🏥 Projeto Web Full-Stack - Gestão de Pacientes para Psicólogos

Este é um projeto **Full-Stack** desenvolvido com **Django** e **SQLite**, permitindo o gerenciamento de pacientes, consultas e registros médicos.

## 📌 Funcionalidades

- 📄 Cadastro e listagem de pacientes.
- 📆 Registro e visualização de consultas.
- 📹 Upload e visualização de vídeos de acompanhamento.
- 📊 Gráficos dinâmicos de humor do paciente.
- 🔑 Controle de acesso a consultas privadas.

## 🛠️ Tecnologias Utilizadas

- **Backend:** Django
- **Banco de Dados:** SQLite
- **Frontend:** HTML + TailwindCSS
- **Bibliotecas:** Pillow, Chart.js

## 🚀 Como Rodar o Projeto Localmente

### 1️⃣ Clonar o Repositório
bash
git clone https://github.com/seu-usuario/seu-repositorio.git
cd seu-repositorio


### 2️⃣ Criar um Ambiente Virtual e Ativar

#### 🔹 Linux
bash
python3 -m venv venv
source venv/bin/activate


#### 🔹 Windows
bash
python -m venv venv
venv\Scripts\Activate


### 3️⃣ Instalar as Dependências
bash
pip install -r requirements.txt


### 4️⃣ Configurar o Banco de Dados
bash
python manage.py migrate


### 5️⃣ Criar um Superusuário (Opcional)
bash
python manage.py createsuperuser


### 6️⃣ Executar o Servidor Localmente
bash
python manage.py runserver

Acesse no navegador: [http://127.0.0.1:8000](http://127.0.0.1:8000)

## 📂 Estrutura do Projeto


/seu-projeto/
│── core/                 # Configuração principal do Django
│── pacientes/            # Aplicação para gerenciar pacientes e consultas
│── static/               # Arquivos estáticos (CSS, JS)
│── templates/            # Templates HTML
│── db.sqlite3            # Banco de dados SQLite
│── manage.py             # Comando de gerenciamento do Django
│── requirements.txt      # Dependências do projeto
│── README.md             # Este arquivo


## 📌 Configuração de Arquivos Estáticos e Mídia

Adicionar no **settings.py**:
python
import os

STATIC_URL = '/static/'
STATICFILES_DIRS = [os.path.join(BASE_DIR, 'templates/static')]
STATIC_ROOT = os.path.join(BASE_DIR, 'static')

MEDIA_URL = '/media/'
MEDIA_ROOT = os.path.join(BASE_DIR, 'media')


Adicionar no **urls.py**:
python
from django.conf import settings
from django.conf.urls.static import static

urlpatterns += static(settings.MEDIA_URL, document_root=settings.MEDIA_ROOT)


## 🎯 Principais URLs

- `http://127.0.0.1:8000/admin/` → Painel de administração.
- `http://127.0.0.1:8000/pacientes/` → Lista de pacientes.
- `http://127.0.0.1:8000/pacientes/ID` → Detalhes de um paciente.
- `http://127.0.0.1:8000/consulta_publica/ID` → Página pública da consulta.

## 📌 Contribuindo

Sinta-se à vontade para contribuir! Clone o projeto, crie uma branch e envie um Pull Request.

## 📜 Licença

Este projeto é de código aberto e pode ser usado conforme necessário.

---
Desenvolvido por **Lucas Lucena ** 🚀

