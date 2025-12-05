# Ambiente SEED Labs em Mac Apple Silicon (M1/M2/M3) com Colima (x86_64)


## 0. Ativar a Rosetta no Docker Desktop

<img src="https://files.fm/thumb_show.php?i=8uxu8sgupe" alt="Ativar Rosetta no Docker Desktop">

## 1. Instalar dependências

```bash
brew install colima qemu
```


```bash
brew install lima-additional-guestagent
# ou
brew install lima-additional-guestagents
```

---

## 2. Iniciar o Colima em x86_64

Iniciar a VM x86_64 emulada, com 4 CPUs e 8 GB de RAM:

```bash
colima start --arch x86_64 --cpu 4 --memory 8
```

Verificar o estado:

```bash
colima status
```

---


## 3. Usar a imagem base dos SEED Labs

Imagem do SEED Labs:

```bash
docker pull handsonsecurity/seed-ubuntu:medium
```

Correr o container com a imagem:

```bash
docker run -it --rm handsonsecurity/seed-ubuntu:medium bash
```
