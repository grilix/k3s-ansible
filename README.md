# Clústers Kubernetes con k3s y ansible

Instala y configura k3s para crear un clúster kubernetes en nodos
corriendo Debian <= 10 o Raspbian 64 bits.

## Requerimientos

- Ansible 2.4.0+
- Authenticación sin contraseña a los nodos a través de SSH.

## Uso

Crea una copia del archivo `inventory/example.yaml` y configúralo
según necesites.

Luego, usa ese archivo para provisionar el cluster:

```bash
ansible-playbook site.yml -i inventory/my-cluster.yaml
```

## Kubeconfig

Esta configuración está pensada para ser usada con
<https://github.com/grilix/k3s-access>. Idealmente tendremos todo en el
mismo repo en algún momento, capaz.

## Contribuciones

Basado en <https://github.com/k3s-io/k3s-ansible>
