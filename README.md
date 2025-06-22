# ParaBank Test Reports

Este repositorio contiene los reportes generados automáticamente por la suite de testing del proyecto [QA_automation_portfolio](https://github.com/darmel/QA_automation_portfolio).

Cada vez que se ejecutan los tests (UI, API o base de datos), se genera un reporte con [Allure](https://docs.qameta.io/allure/), y el contenido se publica automáticamente aquí a través de GitHub + Jenkins + Vercel.

---

## ¿Cómo funciona?

1. Jenkins ejecuta la suite de tests del repositorio principal.
2. Al finalizar, se genera un directorio `allure-report` con los resultados de las ejecuciones.
3. Una post action en el job de jenkins ejecuta un script que realiza:
   - copiar el contenido de "allure-report" a este repositorio (`parabank_tests_reports`).
   - Se hace commit y push automático desde el contenedor.
   - Vercel detecta el cambio y publica el nuevo reporte en segundos.

---

## Acceso al reporte

El último reporte publicado es acesible desde: 

*[Tests Parabank - Allure Report](https://parabank-tests-reports.vercel.app/#)*

---

## Importante

Este repositorio **no contiene código de pruebas**, solo los archivos estáticos generados por Allure. 

---
