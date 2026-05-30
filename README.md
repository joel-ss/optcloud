# optcloud

Ejercicios prácticos de la asignatura de **Cloud**, resueltos con **Terraform**
sobre **AWS**. El repositorio recoge mi trabajo con infraestructura como código
(IaC): definir, desplegar y destruir recursos en la nube de forma reproducible.

![Terraform](https://img.shields.io/badge/Terraform-7B42BC?style=flat&logo=terraform&logoColor=white)
![AWS](https://img.shields.io/badge/AWS-232F3E?style=flat&logo=amazonwebservices&logoColor=white)

## 🛠️ Tecnologías

- **Terraform** (HCL) como herramienta principal de IaC
- **AWS** como proveedor cloud
- Scripts de apoyo en **Bash**

## 📂 Estructura

```
exercicis/   → ejercicios de Terraform, organizados por tema
```

## 🚀 Uso

Cada ejercicio se despliega con el flujo habitual de Terraform. Desde la carpeta
del ejercicio correspondiente:

```bash
terraform init      # descarga el provider de AWS
terraform plan      # revisa los cambios antes de aplicarlos
terraform apply     # crea la infraestructura
terraform destroy   # elimina los recursos al terminar
```

> Requiere una cuenta de AWS con credenciales configuradas (`aws configure` o
> variables de entorno). Acuérdate de ejecutar `terraform destroy` al acabar
> cada ejercicio para no incurrir en costes innecesarios.

## 📝 Contenido

<!-- Opcional: enumera aquí los ejercicios principales para que se entienda el
     alcance de un vistazo. Ejemplos del tipo de temas habituales: -->

- Provisión de instancias EC2
- Redes: VPC, subredes y security groups
- Almacenamiento y otros servicios de AWS

## 📄 Licencia

Distribuido bajo licencia MIT. Ver el archivo `LICENSE` para más detalles.
