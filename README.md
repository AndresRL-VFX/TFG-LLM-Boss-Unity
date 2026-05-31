# TFG: Sistema conversacional controlado por IA en tiempo real

Prototipo en Unity de un jefe final que reacciona a la voz del jugador mediante un Modelo de Lenguaje de Gran Escala (LLM).

**Trabajo Fin de Grado** - Grado en Creación y Narración de Videojuegos
**Universidad Francisco de Vitoria** (2025/2026)

**Autor:** Andrés Rodríguez López
**Tutor:** Pedro Pablo Aulló

---

## Descripción

El sistema integra cuatro tecnologías:

- **Unity (C#)** para el entorno visual, el combate y la captura de audio.
- **Whisper (OpenAI)** para transcribir la voz del jugador a texto.
- **GPT-4o-mini (OpenAI)** para clasificar la intención del mensaje y generar la respuesta del jefe.
- **Text-to-Speech (OpenAI)** para sintetizar la voz hablada del jefe.

La arquitectura sigue un enfoque híbrido por capas: una FSM convencional gestiona la lógica del combate, mientras el LLM actúa como capa modificadora que reacciona al tono de la voz del jugador.

---

## Descargar el prototipo

La build jugable está disponible en la sección **[Releases](../../releases)** de este repositorio.

### Requisitos del sistema

- Windows 10 / 11 (64 bits)
- Micrófono funcional
- Python 3.10 instalado
- Conexión a Internet


### Cómo ejecutarlo

1. Descarga el archivo ZIP desde Releases.
2. Descomprime en una carpeta.
3. Ejecuta el `.exe`.

---

## Cómo funciona

1. El jugador pulsa el botón V y habla durante 5 segundos.
2. Whisper transcribe la voz en local.
3. GPT-4o-mini clasifica la intención del mensaje y elige una de seis acciones del jefe (atacar, bloquear, disparar, curarse, etc.).
4. El jefe ejecuta la animación correspondiente y pronuncia una frase generada por el modelo.

---

## Limitaciones conocidas

- Latencia entre 3 y 5 segundos por interacción.
- Whisper puede fallar al transcribir frases cortas o mal vocalizadas.
- Requiere clave de OpenAI de pago (coste por llamada).

---

## Licencia

Proyecto académico de uso libre con fines educativos.
El uso de la API de OpenAI está sujeto a sus propios términos.
