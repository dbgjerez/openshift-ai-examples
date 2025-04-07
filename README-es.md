# Instalación de OpenShift AI con GitOps

Este repositorio detalla paso a paso cómo realizar la instalación de OpenShift AI en un formato de GitOps, haciendo uso de ArgoCD sobre OpenShift.

## Instalación

La instalación se compone de los siguientes pasos:

> 💡 **Nota**: si ya existe en el cluster alguno de los operadores detallados, dicho paso puede ser omitido.

- Instalación de OpenShift GitOps (ArgoCD)  
- Instalación de ODF (en su defecto, cualquier proveedor de almacenamiento)  
- Instalación de OpenShift AI

### OpenShift GitOps

En el caso de no tener instalado ArgoCD, lo primero que haremos será la instalación del mismo. Para ello, iremos al marketplace y realizaremos la instalación del operador **OpenShift GitOps**.

### OpenShift Data Foundation (ODF)

El caso de ODF es similar. En el caso de no estar instalado en el cluster, procederemos a su instalación a través del marketplace. También puede utilizarse otro proveedor de almacenamiento compatible.

### Bootstrap

Una vez tenemos instalado ArgoCD, aplicaremos la aplicación *bootstrap* de ArgoCD:

```bash
oc apply -f bootstrap
