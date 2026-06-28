# Proyecto: Evals para conocimiento táctico de balonmano

## Objetivo
Sistema de evaluación de respuestas LLM sobre táctica de balonmano (defensa
6-0, 5-1, contraataque, juego posicional). Audiencia asumida del LLM:
entrenadores en formación / categorías base.

## Estado actual
Semana X de 8. Fecha límite de publicación: 23 de agosto de 2026.

## Stack
- Python 3.11+
- Anthropic SDK
- pandas para manipulación de dataset
- JSONL como formato de datos
- pytest para tests

## Estructura
- data/ — dataset de preguntas (JSONL)
- evals/ — sistema de evaluación (judge LLM + métricas)
- src/ — código del proyecto
- notes/ — notas de aprendizaje y retros semanales
- docs/ — documentación pública (case study)

## Convenciones del proyecto
- Nombres de variables en inglés (el código apunta a público internacional)
- Comentarios y docstrings en inglés
- Pero el dataset, rúbrica y respuestas de referencia están en español
  (es parte del valor del proyecto)
- Commits en inglés, mensajes claros y atómicos

## Filosofía de evals (importante)
Este proyecto NO es fact-checking. Las respuestas se evalúan en escala
1-5 sobre 4 dimensiones: corrección técnica, profundidad táctica,
adecuación al nivel, especificidad. Una pregunta puede tener varias
respuestas válidas (campo valid_alternatives en el dataset).

## Qué NO hacer
- No añadir features nuevos no contemplados en el roadmap del ciclo
  (regla 3: nada nuevo hasta publicar)
- No usar datos de Adsmurai bajo ninguna circunstancia
- No mezclar tareas: si Carlos pide "ayúdame con esto", quédate en
  esto, no expandas a "y de paso podríamos...".

## Referencias
- Hamel Husain: hamel.dev/blog/posts/evals/
- Eugene Yan: eugeneyan.com/writing/llm-evaluators/
- Shreya Shankar: sh-reya.com