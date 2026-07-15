# Práctica 2do Parcial - Ansible

## Objetivo

Crear un laboratorio con dos servidores Linux utilizando Docker y administrarlos mediante Ansible, automatizando tareas de configuración en ambos servidores.

---

## Archivos del proyecto

```text
ansible-lab/
├── docker-compose.yml
├── inventory.ini
├── playbook.yml
└── README.md
```

---

## Comandos del Laboratorio

### 1. Iniciar los contenedores
```bash
docker compose up -d
```

### 2. Verificar los contenedores
```bash
docker ps
```

### 3. Comprobar la conexión con Ansible
```bash
ansible docker -i inventory.ini -m ping
```

### 4. Ejecutar el playbook
```bash
ansible-playbook -i inventory.ini playbook.yml
```

---

## Resultado

El playbook realiza las siguientes tareas:

* Muestra el nombre del host.
* Muestra el sistema operativo.
* Crea el directorio `/tmp/ansible-demo`.
* Crea el archivo `info.txt`.
* Guarda el nombre del servidor y el sistema operativo.
* Crea los directorios:
  * `logs`
  * `backup`
  * `config`
* Muestra un mensaje cuando el sistema operativo es Ubuntu.

---

## Captura

<img width="1902" alt="Screenshot 2026-07-14 200953" src="https://github.com/user-attachments/assets/726e02af-043b-4095-a9ad-9320b7f06817" />
