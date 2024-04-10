def media(m,h,t):
    media_cliente = (m + h + t) / 3
    return round(media_cliente, 1)

clientes = []
mercearia = []
higiene = []
talho = []
minimo = 0
n_clientes = int(input("Digite o numero de clientes : "))
for i in range(n_clientes):
    nome= input(f"Insira o nome do cliente {i+1}: ")
    mercado = float(input(f"Insira o dinheiro gasto em mercearia em € do cliente {i+1}: "))
    limpeza = float(input(f"Insira o dinheiro gasto em higiene em € do cliente {i+1}: "))
    tal = float(input(f"Insira o dinheiro gasto em talho em € do cliente {i+1}: "))
    med = media(mercado,limpeza,tal)
    print(f"\nA media do cliente {i+1} é : {med:.1f} \n")
    if mercado < limpeza and mercado < tal:
        print("A menor compra foi no: mercado \n")
    elif limpeza < mercado and limpeza < tal:
        print("A menor compra foi no :limpeza \n")
    else:
        print("A menor compra foi no:talho \n")
   

    clientes.append(nome)
    mercearia.append(mercado)
    higiene.append(limpeza)
    talho.append(tal)

media_mercearia = sum(mercearia) / n_clientes
media_higiene = sum(higiene) / n_clientes
media_talho = sum(talho) / n_clientes


print(f"A média de compras do sector 'mercearia' é : {media_mercearia:.1f}")
print(f"A média de compras do sector 'higiene' é : {media_higiene:.1f}")
print(f"A média de compras do sector 'talho' é : {media_talho:.1f}")
