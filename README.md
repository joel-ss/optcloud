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

Los ejercicios siguen una progresión, de lo más básico a infraestructura de red más completa:

- **[pt1-3 — Primeras instancias EC2 y VPC básica](exercicis/pt1-3)**
  Instancias EC2 con parámetros mínimos (AMI, tipo) y una VPC propia (`10.0.0.0/16`) con varias subredes e instancias dentro.
- **[pt1-4 — Red completa y conectividad](exercicis/pt1-4)**
  VPC y subredes, Internet Gateway, tablas de rutas, Security Groups e instancias, con comprobaciones de acceso SSH y *ping*.
- **[pt1-5 — Meta-argumentos `count` y `for_each`](exercicis/pt1-5)**
  La misma infraestructura resuelta de dos maneras para comparar ambos enfoques: [`count`](exercicis/pt1-5/count) · [`for_each`](exercicis/pt1-5/for_each).
- **[pt1-6 — Bastion host y SSH automatizado](exercicis/pt1-6)**
  Subred pública (bastion) y subredes privadas derivadas con `cidrsubnet`, usando `data`, `locals` y `templatefile`, más un script que configura el acceso SSH a las instancias privadas.

## 📄 Licencia

Distribuido bajo licencia MIT. Ver el archivo `LICENSE` para más detalles.
