# Voice2Text

### Instalación
```bash
pip install SpeechRecognition

pip install PyAudio
```

### Código
```python
import speech_recognition as sr

r = sr.Recognizer()

with sr.Microphone() as source:
    print("Di algunas palabras:")
    audio = r.listen(source)
    try:
        text = r.recognize_google(audio, language='es-AR')
        print("Entendí lo siguiente: {}".format(text))
    except:
        print("Disculpas, no te entendí")
```

### Ejecución
```bash
python index.py
```