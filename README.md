# Istio - Proyecto de Aprendizaje y Ejemplos

## Descripción
Este repositorio contiene ejemplos prácticos y ejercicios para aprender a usar Istio, una plataforma de service mesh que proporciona control sobre el tráfico de red, seguridad, observabilidad y más para aplicaciones basadas en microservicios en Kubernetes.

## Estructura del Proyecto

El repositorio está organizado en varios directorios que representan diferentes aspectos y características de Istio:

- **warmup-exercise/**: Ejercicio inicial para familiarizarse con Istio
- **1-Telemetry/**: Ejemplos de configuración para telemetría y observabilidad
- **2-Traffic-Starting-Files/** y **2-Traffic-Ending-Files/**: Material para gestión de tráfico 
- **3-Gateways-*/**: Diferentes ejemplos y soluciones para la configuración de gateways Istio
- **4-Dark-Releases/**: Implementación de despliegues "dark" o en sombra
- **5-Fault-Injection/**: Ejemplos de inyección de fallas y pruebas de resiliencia
- **6-Circuit-Breaking/**: Implementación de patrones de circuit breaking
- **7-mTLS/**: Configuración de seguridad con mTLS (mutual TLS)
- **8-Customization/**: Personalización de Istio
- **9-Upgrading/**: Proceso de actualización de Istio
- **10-Service-Entries/**: Configuración de service entries para servicios externos
- **envoy_demo/**: Demostración del proxy Envoy
- **no_header_propagation_demo/**: Ejemplo de propagación de encabezados

## Prerrequisitos

- Kubernetes cluster (minikube, Docker Desktop, o plataforma en la nube)
- kubectl configurado
- Istio instalado

## Instrucciones de Uso

Cada directorio contiene archivos YAML y recursos necesarios para implementar diferentes aspectos de Istio. Generalmente, puedes aplicar estos archivos en tu clúster Kubernetes usando:

```bash
kubectl apply -f <archivo.yaml>
```

Para los ejercicios que requieren la instalación de Istio, primero aplica los archivos en este orden:

```bash
kubectl apply -f 1-istio-init.yaml
kubectl apply -f 2-istio-minikube.yaml
kubectl apply -f 3-kiali-secret.yaml
kubectl apply -f 4-label-default-namespace.yaml
```

Luego, despliega la aplicación de demostración:

```bash
kubectl apply -f <archivo-aplicación>.yaml
```

## Aplicación de Demostración

La aplicación de demostración es un sistema de gestión de flotas con varios microservicios:

- position-simulator
- position-tracker
- api-gateway
- webapp
- vehicle-telemetry
- staff-service
- photo-service

Esta aplicación sirve como base para mostrar las capacidades de Istio en un entorno de microservicios real.

## Recursos Adicionales

- [Documentación oficial de Istio](https://istio.io/latest/docs/)
- [Guía de instalación de Istio](https://istio.io/latest/docs/setup/getting-started/)
- [Conceptos de Istio](https://istio.io/latest/docs/concepts/what-is-istio/)
