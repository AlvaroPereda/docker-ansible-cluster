# Ansible + Docker Multinodo Lab

Este proyecto crea un entorno de laboratorio con múltiples contenedores Docker simulando nodos remotos gestionados por Ansible.

---

## 🐳 ¿Qué incluye?

- Un contenedor `ansible-control` que actúa como nodo de control.
- Dos nodos remotos (`node1`, `node2`) accesibles vía SSH en red interna Docker.
- Configuración de inventario estático y playbook de ejemplo.
- Dockerfiles personalizados para control y nodos.

---

## 🚀 Pasos para usarlo

### 1. Levantar el entorno

```
docker compose up --build -d
```
### 2. Acceder al contenedor control

```
docker exec -it ansible-control bash
```
### 3. Verificar conectividad con Ansible

```
ansible all -m ping
```
### 4. Ejecutar el playbook

```
ansible-playbook playbook.yml
```
