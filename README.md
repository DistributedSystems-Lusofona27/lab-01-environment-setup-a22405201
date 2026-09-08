# Lab 1 — Environment Setup

**Nome:** Gonçalo Gonçalves
**Número de estudante:** a22405201

## Ambiente verificado

```
java -version
openjdk version "25.0.4.1" 2026-08-18 LTS
OpenJDK Runtime Environment Temurin-25.0.4.1+1 (build 25.0.4.1+1-LTS)
OpenJDK 64-Bit Server VM Temurin-25.0.4.1+1 (build 25.0.4.1+1-LTS, mixed mode, sharing)
```

```
./mvnw -version
Apache Maven 3.9.16
Java version: 25.0.4.1, vendor: Eclipse Adoptium
```

```
docker compose version
Docker Compose version v2.39.4-desktop.1
```

## Como correr o serviço

```bash
./mvnw spring-boot:run
```

A aplicação arranca na porta 8080.

## Endpoints

| Método | Caminho | Resposta |
|---|---|---|
| GET | `/hello` | `Hello from pt.ulusofona.cd` |
| GET | `/actuator/health` | `{"status":"UP"}` |

## Problemas encontrados

O Docker Desktop não conseguia arrancar o daemon (`HCS_E_HYPERV_NOT_INSTALLED`), mesmo com a
virtualização ativa na BIOS e as features do Windows (WSL2, Virtual Machine Platform) instaladas.
A causa raiz foi o `hypervisorlaunchtype` estar definido como `Off` nas opções de arranque do
Windows (`bcdedit`). Resolvido com:

```powershell
bcdedit /set hypervisorlaunchtype auto
```

seguido de reinício do PC.

