print("Bem-vindo à Loja de Açaí e Cupuaçu!")
print("Desenvolvido por Antonio Rubens Sousa\n")  

total_pedido = 0.0

while True:

    while True:
        sabor = input("Digite o sabor desejado (CP para Cupuaçu / AC para Açaí): ").upper()
        if sabor in ['CP', 'AC']:
            break
        else:
         
            print("Sabor inválido. Tente novamente")
            continue  

    while True:
        tamanho = input("Digite o tamanho desejado (P/M/G): ").upper()
        if tamanho in ['P', 'M', 'G']:
            break
        else:
            print("Tamanho inválido. Tente novamente")
            continue  

    if sabor == 'CP':
        if tamanho == 'P':
            preco = 9.0
        elif tamanho == 'M':
            preco = 14.0
        else:  
            preco = 18.0
    else:  
        if tamanho == 'P':
            preco = 11.0
        elif tamanho == 'M':
            preco = 16.0
        else:  
            preco = 20.0

    total_pedido += preco

   
    print(f"Pedido registrado: {sabor} tamanho {tamanho} - R$ {preco:.2f}")

    
    while True:
        continuar = input("Deseja pedir mais alguma coisa? (S/N): ").upper()
        if continuar in ['S', 'N']:
            break
        else:
            print("Opção inválida. Digite S ou N.")
    
    if continuar == 'N':
        break  

print(f"\nTotal do pedido: R$ {total_pedido:.2f}")
print("Obrigado pela preferência!")
