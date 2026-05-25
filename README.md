# Minttora — Calculadora de Inversión en Oro Tokenizado

Calculadora financiera interactiva de un solo archivo para la plataforma **Minttora**, diseñada para proyectar rendimientos de inversión en oro tokenizado (NFTs).

## Demo

Abre `minttora-calculator.html` directamente en cualquier navegador. No requiere servidor, instalación ni conexión a internet.

---

## Características

- **Calculadora principal** — ingresa cualquier monto y detecta el paquete automáticamente
- **Simulador de retiro** — proyecta cuánto recibirías al retirar en cualquier fecha
- **Tabla de proyección** — vista mensual o semanal de toda la duración del NFT
- **Tarjetas de ejemplo** — presets rápidos para $100, $500, $2,000 y $50,000
- **Tabla comparativa** — los 4 paquetes en paralelo con todos sus datos
- **Botón WhatsApp** — comparte el resultado de tu inversión

---

## Paquetes disponibles

| Paquete | Rango de inversión | Rendimiento diario | Duración estimada |
|---------|-------------------|-------------------|-------------------|
| Inicial | $30 – $999        | 0.60% (días hábiles) | ~24 meses      |
| Bronce  | $1,000 – $9,999   | 0.65% (días hábiles) | ~22 meses      |
| Plata   | $10,000 – $29,999 | 0.70% (días hábiles) | ~21 meses      |
| Oro     | $30,000+          | 0.75% (días hábiles) | ~19 meses      |

> Los rendimientos se acumulan de lunes a viernes (días hábiles).  
> El NFT finaliza cuando las ganancias acumuladas alcanzan el **300% del capital original invertido**.

---

## Reglas de negocio

- **Fee de depósito:** 1% deducido al invertir  
- **Fee de retiro:** 3% deducido sobre cualquier retiro  
- **Meta del NFT:** ganancias = 300% del monto original (no duración fija)  
- **Días hábiles:** lunes a viernes (se excluyen sábado y domingo)

### Cálculo de duración

```
Capital neto = inversión × 0.99
Ganancia diaria = capital neto × tasa del paquete
Días hasta 300% = ceil((inversión × 3) / ganancia diaria)
```

---

## Estructura del proyecto

```
minttora-calculator.html   ← Archivo único, todo incluido (HTML + CSS + JS + logo)
README.md                  ← Este archivo
```

---

## Uso en GitHub Pages

1. Ve a **Settings → Pages** en tu repositorio
2. Selecciona la rama `main` y carpeta `/ (root)`
3. Guarda — tu calculadora estará disponible en `https://tu-usuario.github.io/nombre-repo/minttora-calculator.html`

---

## Tecnologías

- HTML5 / CSS3 / JavaScript vanilla — sin frameworks ni dependencias externas
- Fuentes: [Syne](https://fonts.google.com/specimen/Syne) + [Space Grotesk](https://fonts.google.com/specimen/Space+Grotesk) (Google Fonts)
- Logo Minttora embebido en base64 (archivo completamente autocontenido)

---

*Calculadora desarrollada para uso informativo. Los rendimientos son aproximados y pueden variar entre 8–15% mensual según condiciones del mercado.*
