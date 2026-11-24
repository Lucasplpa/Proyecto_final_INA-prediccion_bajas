# Informe de ética

**Proyecto:** Predicción de bajas voluntarias de empleados

## 1. Origen de los datos
Se usa el dataset público *IBM HR Analytics Employee Attrition*, publicado por IBM y difundido en Kaggle. Contiene **datos ficticios**, creados con fines educativos: no corresponden a personas reales.

## 2. Privacidad
Si el modelo se aplicara con datos reales de empleados, habría que cumplir la **Ley 25.326 de Protección de Datos Personales**:
- Usar los datos solo para la finalidad informada (retención), no para otros fines.
- Anonimizar o seudonimizar los registros durante el análisis.
- Restringir el acceso a los resultados a personas autorizadas de RRHH.
- Informar a los empleados que sus datos se usan para este análisis.

## 3. Sesgo y no discriminación
- Se **excluyeron** edad, género y estado civil para que el modelo no discrimine por esas características. La Ley de Contrato de Trabajo (art. 17) prohíbe discriminar entre trabajadores, entre otros motivos, por sexo o edad.
- Se probó el modelo con esas variables (anexo del notebook): la exactitud sube de 75,5% a 77,6% por tener menos falsas alarmas, pero detecta **menos** bajas (32 vs. 35 de 47). La mejora no compensa el riesgo.
- Uso legítimo de estas variables: **auditar** el modelo (verificar que no trate peor a un grupo) o analizar tendencias agregadas, nunca como entrada para calificar a una persona.
- **Limitación:** algunas variables usadas (por ejemplo, años de experiencia) se relacionan con la edad, por lo que el sesgo se reduce pero no desaparece. Antes de un uso real se debería revisar el resultado por grupos.

## 4. Uso responsable
- El modelo es una **herramienta de apoyo**: sirve para priorizar conversaciones de retención, no para tomar decisiones automáticas.
- **No debe usarse** para despedir, negar promociones ni sancionar a una persona.
- Toda alerta debe ser revisada por una persona de RRHH, que es quien decide.

## 5. Limitaciones del modelo
- De 95 alertas en los datos de prueba, 60 fueron falsas alarmas. Una alerta **no** significa que la persona se va a ir.
- No detectó 12 de las 47 bajas reales.
- Al ser datos ficticios, los resultados no se pueden trasladar directamente a una empresa real.

## 6. Responsabilidad social
Bien usado, el modelo puede mejorar la experiencia de los empleados: las variables más asociadas a las bajas (horas extra, baja satisfacción, nivel inicial) señalan condiciones de trabajo que la empresa puede mejorar, no "culpas" individuales.
