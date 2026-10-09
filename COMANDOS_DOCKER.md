# Atividade - Introdução ao Docker

## 1. Verificar se o Docker está instalado
```bash
docker --version
```

## 2. Entrar na pasta do projeto
Abra o terminal dentro da pasta `teste-github-actions-main`, onde está o Dockerfile.

## 3. Criar a imagem
```bash
docker build -t calculadora-aula .
```

## 4. Conferir a imagem criada
```bash
docker images
```

## 5. Criar e executar o container (os testes são executados dentro dele)
```bash
docker run --name calculadora-container calculadora-aula
```

O comando executa os testes com pytest. Ao terminar, o container para normalmente.

## 6. Conferir o container
```bash
docker ps -a
```

## 7. Ver o resultado/logs do container
```bash
docker logs calculadora-container
```

## 8. Remover o container (opcional)
```bash
docker rm calculadora-container
```

## 9. Executar novamente os testes criando um container novo
```bash
docker run --rm calculadora-aula
```

Observação: esta aplicação é uma calculadora em Python sem interface web. O container executa os testes automatizados do projeto e termina quando eles acabam.
