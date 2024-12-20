Nesse arquivo, criei um codigo para controle de estoque. Usando o python como linguagem.

importar pandas como pd

def add_item(estoque, nome_item, quantidade, preço):
  """Adiciona um item ao inventário ou atualiza a quantidade existente."""
  se item_name estiver no inventário:
    inventário[item_name]['quantidade'] += quantidade
  outro:
    inventário[item_name] = {'quantidade': quantidade, 'preço': preço}
  devolver estoque


def remove_item(estoque, nome_item, quantidade):
  """Remove um item do inventário."""
  se item_name estiver no inventário:
    se inventário[item_name]['quantidade'] >= quantidade:
      inventário[item_name]['quantidade'] -= quantidade
      se inventário[item_name]['quantidade'] == 0:
        del inventário[item_name] # remove o item se a quantidade for 0
      devolver estoque
    outro:
      print(f"Não há {item_name} suficiente em estoque.")
      devolver estoque
  outro:
    print(f"{item_name} não encontrado no inventário.")
    devolver estoque


def view_inventory(inventário):
  """Exibe o inventário atual."""
  se não for inventário:
    print("O estoque está vazio.")
    retornar

  df = pd.DataFrame.from_dict(inventário, orientar='índice')
  imprimir (df)


# Exemplo de uso:
inventário = {}

inventário = add_item(inventário, "Laptop", 10, 1200)
inventário = add_item(inventário, "Mouse", 20, 25)
inventário = add_item(inventário, "Teclado", 15, 75)

view_inventory(inventário)


inventário = remove_item(inventário, "Laptop", 5)
view_inventory(inventário)

inventário = remove_item(inventory, "Monitor", 2) # Exemplo de tentativa de remover um item que não está no inventário

inventário = remove_item(inventory, "Mouse", 25) # Exemplo de tentativa de remover mais itens do que os disponíveis
```# Projetos.Diversos
Projetos variados
