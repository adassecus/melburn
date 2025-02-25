# Meloburn 0.7 🍯🎶

O **Meloburn 0.7** é um aplicativo gráfico desenvolvido em Python para organizar sua biblioteca musical de forma prática e inteligente. Este README.md contém todas as informações necessárias para compreender, configurar e utilizar o programa, sem necessidade de arquivos adicionais.

---

## Visão Geral

- **Organização de Músicas:** Separa os arquivos musicais por artista e álbum.
- **Renomeação e Numeração de Faixas:** Corrige os metadados e padroniza os nomes dos arquivos, facilitando a navegação em aparelhos de som.
- **Otimização para Pen Drives:** Oferece duas opções de operação:
  - **Formatar o pen drive (🔥):** Apaga todo o conteúdo antes de copiar as músicas.
  - **Adicionar músicas (➕):** Copia novas músicas sem apagar o conteúdo já existente.
- **Exibição de Logs Detalhados:** Acompanha todo o processo com mensagens interativas.
- **Busca de Metadados (Opcional):** Utiliza a API do [TheAudioDB](https://www.theaudiodb.com/) para identificar automaticamente artistas e títulos. Se a API não for configurada, os metadados não identificados serão marcados como **"Desconhecido"**.

---

## Funcionalidades

- **Interface Gráfica com Tkinter:** Simples, intuitiva e elegante.
- **Verificação de Privilégios Administrativos:** Garante que o script seja executado com as permissões necessárias para operações de sistema, como a formatação do pen drive.
- **Busca de Metadados Opcional:**  
  Acesse o site da [TheAudioDB](https://www.theaudiodb.com/) para obter sua chave de API. Caso deseje que o script busque automaticamente os metadados, insira sua chave nas funções `lookup_artist_by_track` e `lookup_track_by_artist` no arquivo `melburnwin.py`. Se a chave não for configurada, os metadados não identificados serão definidos como **"Desconhecido"**.
- **Monitoramento do Progresso:** Barra de progresso e logs em tempo real durante a cópia dos arquivos.
- **Exportação de Logs:** Permite salvar o registro das operações para consulta futura.

---

## Requisitos e Dependências

### Sistema Operacional
- **Windows:** Desenvolvido e testado para Windows 10 ou superior.  
  *Observação:* É necessário executar o script com privilégios de administrador.

### Softwares e Bibliotecas
- **Python 3.x** – [Download Python](https://www.python.org/downloads/)
- **Tkinter:** Geralmente incluído com o Python em ambientes Windows.
- **Mutagen:** Para manipulação de metadados.  
  ```bash
  pip install mutagen
  ```
- **Requests:** Para realizar requisições HTTP.  
  ```bash
  pip install requests
  ```

---

## Instalação e Configuração

### 1. Obtenha o Arquivo

O script está disponível para download direto como um único arquivo chamado `melburnwin.py` neste mesmo diretório. Para baixar:
   - Clique no arquivo `melburnwin.py` no repositório.
   - Selecione a opção **Raw** e salve o arquivo (Ctrl+S) em seu computador.

### 2. (Opcional) Crie um Ambiente Virtual

Abra o **Prompt de Comando** e execute:
```bash
python -m venv venv
venv\Scripts\activate
```

### 3. Instale as Dependências

Instale as bibliotecas necessárias com os seguintes comandos:
```bash
pip install mutagen requests
```

### 4. Configuração da API (Opcional)

Para que o script possa buscar e corrigir metadados automaticamente:
- Acesse o site da [TheAudioDB](https://www.theaudiodb.com/) e registre-se para obter sua chave de API.
- No arquivo `melburnwin.py`, localize as funções `lookup_artist_by_track` e `lookup_track_by_artist`.
- Substitua o valor padrão `2` na URL pela sua chave de API.  

  **Exemplo:**
  ```python
  API_KEY = "SUA_CHAVE_AQUI"
  url = f"https://theaudiodb.com/api/v1/json/{API_KEY}/searchtrack.php?t={track_title}"
  ```
- Se a chave não for configurada, os metadados não identificados serão definidos como **"Desconhecido"**.

### 5. Permissões Administrativas

**Importante:** Para a formatação do pen drive e outras operações de sistema, o script deve ser executado com privilégios de administrador.  
- Clique com o botão direito no **Prompt de Comando** e selecione “Executar como administrador” antes de iniciar o script.

---

## Como Utilizar

### Opção 1: Executando sem Linha de Comando

Se preferir, você pode abrir o script sem precisar do Prompt de Comando:
1. Clique com o botão direito no arquivo `melburnwin.py`.
2. Selecione **Abrir com...** e escolha **Python**.
3. O programa abrirá a interface gráfica automaticamente.

### Opção 2: Executando pelo Prompt de Comando

1. Abra o **Prompt de Comando** ou **PowerShell**.
2. Navegue até o diretório onde o arquivo `melburnwin.py` foi salvo:
   ```bash
   cd caminho\para\o\diretório
   ```
3. Execute o script:
   ```bash
   python melburnwin.py
   ```
   Isso abrirá a interface gráfica do Meloburn.

### Utilizando a Interface Gráfica

- **Seleção de Pastas:**
  - **Pasta com as músicas:** Selecione a pasta raiz que contém todos os seus arquivos musicais (mesmo que distribuídos em subpastas).
  - **Pen drive:** Escolha a unidade correspondente ao seu pen drive.
  
- **Opções de Operação:**
  - **Formatar pen drive (🔥):** Apaga todo o conteúdo do pen drive antes de copiar as músicas.
  - **Adicionar músicas (➕):** Copia novas músicas sem apagar o conteúdo já existente.
  
- **Iniciar o Processo:**
  - Clique em **"Iniciar Organização 🚀"** e acompanhe o progresso através da barra e dos logs exibidos.
  
- **Exportar Logs:**
  - Ao término do processo, utilize o botão **"Exportar Log 📄"** para salvar o registro das operações.

---

## Contato

Para dúvidas, sugestões ou problemas, entre em contato:

📩 **[t.me/adassecus](https://t.me/adassecus)**
