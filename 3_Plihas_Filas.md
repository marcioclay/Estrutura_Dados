# Pilhas e Filas
Pilhas (Stacks) e Filas (Queues) são estruturas de dados lineares fundamentais. 
A principal diferença entre elas está na ordem de acesso aos elementos.

## 1. Pilhas (Stacks) - Conceito LIFOO algoritmo funciona no modelo LIFO (Last In, First Out). 
O último elemento a entrar é o primeiro a sair. Operações Principais Push: Insere um elemento no topo.Pop: Remove o elemento do topo.Implementação Ideal em PythonPara pilhas, a estrutura nativa list é eficiente. As operações no final da lista funcionam em tempo constante O(1).

### Inicialização
pilha = []

# Push: Adiciona elementos no topo
```
pilha.append("Contexto A")
pilha.append("Contexto B")
pilha.append("Contexto C")
print(f"Pilha após inserções: {pilha}")
```

# Pop: Remove o elemento do topo
```
elemento_removido = pilha.pop()
print(f"Elemento removido: {elemento_removido}")
print(f"Pilha atual: {pilha}")
```

# Peek: Olhar o topo sem remover
topo = pilha[-1] if pilha else None
print(f"Elemento no topo: {topo}")
Use o código com cuidado.2. Filas (Queues) - Conceito FIFOO algoritmo funciona no modelo FIFO (First In, First Out). O primeiro elemento a entrar é o primeiro a sair.Operações PrincipaisEnqueue: Insere um elemento no final da fila.Dequeue: Remove o elemento do início da fila.Implementação Ideal em PythonNão use list para filas. Remover o primeiro elemento de uma lista (list.pop(0)) exige deslocar todos os outros elementos na memória, gerando complexidade de tempo linear O(n).Utilize collections.deque (double-ended queue), que garante inserções e remoções nas extremidades em O(1).pythonfrom collections import deque

# Inicialização
fila = deque()

# Enqueue: Adiciona elementos no final
fila.append("Requisição 1")
fila.append("Requisição 2")
fila.append("Requisição 3")
print(f"Fila após inserções: {list(fila)}")

# Dequeue: Remove o primeiro elemento da fila
elemento_atendido = fila.popleft()
print(f"Elemento atendido: {elemento_atendido}")
print(f"Fila atual: {list(fila)}")
Use o código com cuidado.Summary ComparativoEstruturaPrincípioMétodo de InserçãoMétodo de RemoçãoComplexidade (Ideal)Caso de Uso ComumPilhaLIFOappend()pop()O(1)Histórico (Ctrl+Z), Chamadas de funçãoFilaFIFOappend()popleft()O(1)Processamento de tarefas, Buffers de rede
