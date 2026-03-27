# 📊 Stress Test de Cartera de Crédito: León 2026
### Análisis de Riesgo Crediticio ante Choques Inflacionarios y Canasta Básica

Este proyecto utiliza **Data Science** y **Modelado Financiero** para evaluar la resiliencia de una cartera de **100,000 socios** en León, Guanajuato, frente a un escenario de estrés macroeconómico en marzo de 2026.

## 🎯 Objetivo
Determinar el impacto de un **DTI (Debt-to-Income) del 30%** y una inflación quincenal de **0.62%** sobre la capacidad de pago de la base operativa (industria automotriz y del calzado), considerando el costo real de la canasta básica de **CONEVAL ($4,877.87)**.

---

## 🛠️ Metodología y Datos
- **Muestra:** 100,000 registros sintéticos basados en la distribución salarial de León (ENOE).
- **Filtro de Bancarización:** Se excluyeron ingresos menores a **$4,800** (pobreza extrema).
- **Ingreso Integral:** Se aplicó un ajuste del **12% por vales de despensa** y prestaciones a ingresos menores a $9,500.
- **Variables de Estrés:** Canasta básica ajustada mensualmente + Cuotas de crédito patrimonial.

---

## 📈 Visualización de Resultados

### 1. Perfil Salarial de la Población
La distribución muestra un sesgo hacia la izquierda, reflejando que la mayoría de los socios son trabajadores operativos. La **Mediana Integral ($10,308)** incluye el ajuste de vales de despensa.

<img width="902" height="566" alt="image" src="https://github.com/user-attachments/assets/cb06e9ad-745a-490a-a0dd-31fd078dc32e" />


### 2. Estatus de Salud de la Cartera
El modelo clasifica a los socios en tres categorías según su excedente financiero tras pagar comida y deuda:
- **Sano:** Excedente > $1,000.
- **Riesgo Crítico:** Excedente entre $0 y $1,000.
- **Mora Técnica:** Ingreso insuficiente para cubrir necesidades básicas y crédito.

<img width="777" height="550" alt="image" src="https://github.com/user-attachments/assets/2e28d651-3b85-4081-b781-f83d8df64d34" />


### 3. Probabilidad de Default (PD) por Decil
El análisis por deciles revela que el riesgo no es lineal. El **Decil 0 y 1** concentran la mayor vulnerabilidad, demostrando que el estándar bancario del 30% de DTI es insostenible para estos niveles de ingreso en entornos inflacionarios.

<img width="854" height="565" alt="image" src="https://github.com/user-attachments/assets/598e3be1-e8e4-4475-a100-7b64e04b8192" />


---

## 🔍 Conclusiones Estratégicas
1. **Punto de Ruptura:** Los socios con ingresos menores a **$8,500** presentan una probabilidad de default superior al 30% cuando su deuda alcanza el 30% de su ingreso integral.
2. **Efecto Inflación:** El incremento de la canasta básica actúa como un "impuesto regresivo" que reduce el margen de maniobra de la clase trabajadora de León a menos de **$1,000 MXN mensuales**.
3. **Recomendación de Política:** Implementar un **DTI Diferenciado**. Limitar el endeudamiento al **20%** para los Deciles 0-1 y permitir el **30-35%** solo a partir del Decil 3 ($11,500+).

---

## 💻 Tecnologías Utilizadas
- **Python 3.x**
- **Pandas** (Procesamiento de datos)
- **NumPy** (Simulación estocástica)
- **Matplotlib / Seaborn** (Visualización avanzada)

---
**Escenario:** Marzo 2026 | León, Gto.
