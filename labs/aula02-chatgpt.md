# Guia Prático --- Importar VM Ubuntu Server 22.04.4 LTS no Oracle VirtualBox 7.2

Curso Livre: Inteligência Artificial Voltada a Redes de Computadores\
Instituição: SENAC São Paulo -- Unidade Lapa Tito

## Objetivo

Importar a imagem `UbuntuServer-OnPremises.ova`, configurar a rede em
**Modo Bridge (Ponte)** usando a rede local `10.24.82.0/24` e iniciar a
máquina virtual para acesso remoto via SSH.

------------------------------------------------------------------------

## 🖥️ Informações do Laboratório

-   Sistema Operacional: Microsoft Windows 11
-   Processador: Intel Core i7-14700K
-   Memória RAM: 32 GB
-   Armazenamento: HD 10 TB
-   Virtualizador: Oracle VirtualBox 7.2
-   Arquivo da VM: `UbuntuServer-OnPremises.ova`
-   Local do arquivo: `Downloads`

------------------------------------------------------------------------

# 📥 Etapa 1 --- Abrir o Oracle VirtualBox

1.  Clique no menu **Iniciar**
2.  Pesquise por **Oracle VirtualBox**
3.  Clique para abrir

Resultado esperado:

✅ VirtualBox aberto

------------------------------------------------------------------------

# 📦 Etapa 2 --- Importar a Máquina Virtual

1.  No menu superior clique em:

**Arquivo → Importar Appliance**

2.  Clique no ícone:

📁 **Selecionar arquivo**

3.  Acesse:

`Downloads`

4.  Selecione:

`UbuntuServer-OnPremises.ova`

5.  Clique:

**Próximo**

------------------------------------------------------------------------

# ⚙️ Etapa 3 --- Revisar configurações

Verifique:

-   Nome da VM: UbuntuServer-OnPremises
-   CPU: manter padrão
-   Memória RAM: manter padrão

Clique:

**Concluir / Importar**

Aguarde a importação.

Resultado esperado:

✅ Máquina virtual criada no VirtualBox

------------------------------------------------------------------------

# 🌐 Etapa 4 --- Configurar Rede Bridge (Ponte)

1.  Selecione a máquina virtual

2.  Clique:

**Configurações**

3.  Clique em:

**Rede**

4.  Em Adaptador 1:

Marque:

☑ Habilitar Placa de Rede

5.  Em:

**Conectado a:**

Escolha:

**Adaptador em Ponte (Bridge Adapter)**

6.  Em:

**Nome**

Selecione a placa de rede física cabeada do laboratório

Exemplo:

`Intel Ethernet`

ou

`Realtek Ethernet`

7.  Mantenha:

-   Modo Promíscuo → Permitir Tudo
-   Cabo conectado → marcado

Clique:

**OK**

Resultado esperado:

✅ VM ligada diretamente à rede do laboratório

Rede utilizada:

`10.24.82.0/24`

------------------------------------------------------------------------

# ▶️ Etapa 5 --- Iniciar a Máquina Virtual

1.  Selecione a VM

2.  Clique:

🟢 **Iniciar**

Aguarde o carregamento do Ubuntu Server

Resultado esperado:

✅ Tela de login do Ubuntu Server

------------------------------------------------------------------------

# 🔍 Etapa 6 --- Descobrir endereço IP

Após o login execute:

``` bash
ip a
```

ou:

``` bash
hostname -I
```

Exemplo de retorno:

``` bash
10.24.82.50
```

Anote o IP.

------------------------------------------------------------------------

# 🔐 Etapa 7 --- Acesso remoto SSH

No Windows:

1.  Abra:

**Prompt de Comando**

ou

**PowerShell**

2.  Execute:

``` bash
ssh usuario@IP_DA_VM
```

Exemplo:

``` bash
ssh aluno@10.24.82.50
```

3.  Digite:

`yes`

4.  Informe a senha

Resultado esperado:

✅ Acesso remoto SSH realizado

------------------------------------------------------------------------

# ✅ Checklist Final

☑ VirtualBox aberto

☑ Arquivo OVA importado

☑ Máquina virtual criada

☑ Rede configurada em Bridge

☑ VM iniciada

☑ Endereço IP identificado

☑ SSH funcionando

------------------------------------------------------------------------

Fim do procedimento.
