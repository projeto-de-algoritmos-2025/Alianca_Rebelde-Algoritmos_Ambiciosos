# Aliança Rebelde - Operações Críticas: Manual de Instalação e Execução


## Alternativa:

É possível baixar o jogo ao fazer um git clone do repositório na sua máquina e baixar a pasta com os códgos [Alianca_Rebelde](https://github.com/projeto-de-algoritmos-2025/Alianca_Rebelde-Algoritmos_Ambiciosos/tree/main/Alianca_Rebelde) 

## Instalação 

#### 1. Pré-requisitos

Antes de começar, certifique-se de que você tem os seguintes softwares instalados:

* **Python 3:** O jogo foi desenvolvido usando Python 3 (versão 3.7 ou superior é recomendada). Você pode baixar o Python em [python.org](https://www.python.org/downloads/).
    * Durante a instalação no Windows, marque a opção "Add Python to PATH" ou similar.
* **Git:** Necessário para clonar o repositório do jogo. Você pode baixar o Git em [git-scm.com](https://git-scm.com/downloads).
* **Tkinter:** Esta é a biblioteca gráfica que o jogo utiliza.
    * **Windows e macOS:** Geralmente, o Tkinter já vem instalado com o Python.
    * **Linux:** Se não estiver instalado, você pode instalá-lo usando o gerenciador de pacotes da sua distribuição. Por exemplo, em sistemas baseados em Debian/Ubuntu:
        ```bash
        sudo apt-get update
        sudo apt-get install python3-tk
        ```

#### 2. Configuração do Jogo

Siga os passos abaixo para configurar o jogo no seu computador:

##### a. Clonar o Repositório:

Abra o seu terminal ou prompt de comando e navegue até o diretório onde você deseja salvar o jogo. Em seguida, clone o repositório do GitHub com o seguinte comando (substitua `SEU_USUARIO_GITHUB/NOME_DO_REPOSITORIO` pelo link correto do seu projeto):

```bash
git clone [https://github.com/SEU_USUARIO_GITHUB/NOME_DO_REPOSITORIO.git](https://github.com/SEU_USUARIO_GITHUB/NOME_DO_REPOSITORIO.git)
```

sso criará uma pasta com o nome do repositório contendo todos os arquivos do jogo. Acesse essa pasta:

```bash
cd NOME_DO_REPOSITORIO
```

##### b. (Opcional, mas Recomendado) Criar um Ambiente Virtual:

Usar um ambiente virtual é uma boa prática para isolar as dependências do projeto.

```bash
python3 -m venv venv_alianca_rebelde
```

Ative o ambiente virtual:

#### No Windows:

```bash.\venv_alianca_rebelde\Scripts\activate
```

#### No macOS e Linux:

```bash
source venv_alianca_rebelde/bin/activate
```

Você saberá que o ambiente virtual está ativo porque o nome dele aparecerá no início do seu prompt do terminal.

#### 3. Estrutura de Pastas Esperada
Para que o jogo funcione corretamente, especialmente o carregamento de imagens e módulos, ele espera a seguinte estrutura de pastas dentro do diretório principal do projeto:

      NOME_DO_REPOSITORIO/
      ├── main.py                     # Arquivo principal para executar o jogo
      ├── algoritmos/                 # Pasta para os algoritmos
      │   ├── __init__.py
      │   ├── coin_changing_guloso.py
      │   ├── grafo_bfs.py
      │   ├── interval_partitioning_guloso.py
      │   ├── interval_scheduling_guloso.py
      │   ├── knapsack_fracionario.py
      │   ├── scheduling_minimize_lateness.py
      │   └── union_find.py
      ├── missoes/                    # Pasta para as missões e minigames
      │   ├── __init__.py
      │   ├── missao1.py
      │   ├── missao2.py
      │   ├── missao3.py
      │   ├── missao4.py
      │   ├── missao5.py
      │   ├── minigame_bfs_extração.py  # Verifique o nome exato do arquivo
      │   └── minigame_rpg_kruskal.py # Verifique o nome exato do arquivo
      ├── assets/                     # Pasta para recursos gráficos e sonoros
      │   └── images/
      │       └── Alianca_Rebelde.png # Imagem do símbolo da Aliança
      │       └── fundo_espacial.png  # Exemplo de imagem de fundo para a janela
      └── README.md                   # Este arquivo de manual


#### 4. Como Rodar o Jogo

Depois de clonar o repositório e (opcionalmente) ativar o ambiente virtual:

Navegue pelo terminal até a pasta raiz do projeto (onde o arquivo main.py está localizado).

Execute o jogo com o seguinte comando:

```bash
python3 main.py
```
(Ou python main.py dependendo da sua configuração do Python).

Isso deve iniciar a janela do jogo "Aliança Rebelde - Operações Críticas".

#### 5. Solução de Problemas Comuns

* **`ModuleNotFoundError: No module named 'missoes'` (ou similar):**
    * Certifique-se de que você está executando o `main.py` de dentro da pasta raiz do projeto.
    * Verifique se as pastas `missoes/` e `algoritmos/` existem e contêm um arquivo `__init__.py` (mesmo que vazio) cada uma.

* **Tkinter não encontrado / Erro ao importar `tkinter`:**
    * Consulte a seção "1. Pré-requisitos" para instalar o `python3-tk` (ou equivalente) no seu sistema.

* **Imagens não aparecendo:**
    * Verifique se o nome e o caminho do arquivo da imagem no código (em `main.py` ou nos arquivos de missão) correspondem exatamente ao nome e localização do arquivo de imagem no seu sistema (lembre-se que nomes de arquivo são sensíveis a maiúsculas/minúsculas no Linux).
    * Certifique-se de que as imagens estão em um formato compatível (`.png` ou `.gif` para `PhotoImage` nativo do Tkinter). Se estiver usando outros formatos como `.jpg`, você precisará da biblioteca `Pillow` (veja a seção de instalação de bibliotecas).

* **Problemas de Estilo/Cores:**
    * A aparência dos widgets `ttk` pode variar um pouco dependendo do seu sistema operacional e tema ativo. As configurações de estilo no jogo tentam criar uma experiência consistente, mas podem haver pequenas diferenças visuais.


