# servidor_web
## EQUIPE: 
ANTONIO ALAN / ADENILSON SILVA /  CAYMI FERREIRA / HEBERT IVISSON

Este repósitorio foi desenvolvido para soluncionar o desafio de criar servidor web básico utilizando socktes. [Mais informações sobre o desafio](https://codingchallenges.fyi/challenges/challenge-webserver/).

### Iniciar Servidor no modo assícrono: 
```python
  python servidor_asc.py
```
*Exemplo de uso:*

![image](https://github.com/user-attachments/assets/d083faa3-d15e-418f-859f-beff8b8dcdde)

### Iniciar Servidor no modo multhread  
```python
  python servidor.py -t
```

![image](https://github.com/user-attachments/assets/bb72ab7d-33e6-4468-864e-cddd4f7d746a)

### Iniciar Servidor no modo multiprocessamento
```python
  python servidor.py -p
```
![image](https://github.com/user-attachments/assets/4961bab4-c1d3-47d2-a3ad-2df523ebdde4)

### Fazendo solicitação ao servidor
```python
  python cliente.py 127.0.0.1 2000 "GET / HTTP/1.1`r`nHost: 127.0.0.1`r`n`r`n"
```

OU

```python
  curl http://localhost:2000
```

### Teste de conexões simultâneas ao servidor para tarefas vinculadas a CPU
```python
  python teste_servidor.py -c -nc 5 127.0.0.1 2000
```

### Teste de conexões simultâneas ao servidor para tarefas vinculadas a I/O
```python
  python teste_servidor.py -i -nc 5 127.0.0.1 2000
```

### Teste de erro de porta incorreta
```python
  python cliente.py 127.0.0.1 2001 "GET / HTTP/1.1`r`nHost: 127.0.0.1`r`n`r`n"
```

