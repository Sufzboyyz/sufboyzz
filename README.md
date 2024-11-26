import os

def contar_palavras(arquivo):
    """Conta o número de palavras em um arquivo de texto."""
    if not os.path.exists(arquivo):
        print(f"Arquivo '{arquivo}' não encontrado.")
        return 0

    with open(arquivo, 'r', encoding='utf-8') as f:
        conteudo = f.read()

    palavras = conteudo.split()
    return len(palavras)

if __name__ == "__main__":
    caminho_arquivo = "arquivos/exemplo.txt"
    total_palavras = contar_palavras(caminho_arquivo)
    print(f"O arquivo '{caminho_arquivo}' contém {total_palavras} palavras.")
