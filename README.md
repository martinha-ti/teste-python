# teste-python
Apenas um teste de Python

Vou te mostrar como usar o PyAutoGUI para automatizar uma busca no ChatGPT por 3 comandos em Python com exemplos de código. Vou criar um exemplo de script em Python que simula a entrada do usuário para realizar essa pesquisa.

Aqui está o script:

python
Copiar código
import pyautogui
import time

def open_browser_and_search():
    # Abre o navegador
    pyautogui.hotkey('win', 'r')
    time.sleep(1)
    pyautogui.write('chrome\n', interval=0.1)
    time.sleep(3)  # Aguarda o navegador abrir

    # Acessa o site do ChatGPT (substitua pela URL correta do ChatGPT)
    url = 'https://chat.openai.com'
    pyautogui.write(url + '\n', interval=0.1)
    time.sleep(5)  # Aguarda a página carregar

    # Clica na barra de pesquisa do ChatGPT
    # Aqui você deve ajustar a posição do clique de acordo com a sua tela
    search_box_position = (400, 400)  # Exemplo, ajuste conforme necessário
    pyautogui.click(search_box_position)
    time.sleep(1)

    # Escreve a pergunta no ChatGPT
    search_query = "Me mostre 3 comandos em Python com exemplo de código"
    pyautogui.write(search_query + '\n', interval=0.1)
    time.sleep(5)  # Aguarda a resposta do ChatGPT

if __name__ == "__main__":
    open_browser_and_search()
Passos para executar o script:

Instalar o PyAutoGUI: Certifique-se de que o PyAutoGUI está instalado. Você pode instalá-lo usando pip:

bash
Copiar código
pip install pyautogui
Ajustar posições: O script acima contém posições de cliques que podem não ser precisas para a sua tela. Use o seguinte script para descobrir as coordenadas corretas:

python
Copiar código
import pyautogui
print(pyautogui.position())
Execute este script e mova o mouse sobre a barra de pesquisa do ChatGPT para obter as coordenadas corretas. Atualize o valor de search_box_position no script principal com essas coordenadas.

Executar o script: Salve o script principal em um arquivo, por exemplo, search_chatgpt.py, e execute:

bash
Copiar código
python search_chatgpt.py
Nota Importante:

Este script é um exemplo simples de automação e pode precisar de ajustes dependendo do layout específico do site e das configurações do seu sistema.
Automação de navegação web pode ser sujeita a restrições dependendo dos termos de serviço do site que você está acessando. Use com responsabilidade.
Espero que isso ajude! Se precisar de mais alguma coisa, é só falar.
