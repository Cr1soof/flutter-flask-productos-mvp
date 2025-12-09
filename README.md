# flutter-flask-productos-mvp

4.1. Descripción del proyecto

Breve explicación:

Qué hace la API Flask (CRUD de productos + imágenes).

Qué hace la app Flutter (lista, crea, edita, elimina productos consumiendo la API).

4.2. Requisitos para ejecutar

Backend:

Python 3.x

Flask, Flask-SQLAlchemy, Werkzeug, etc.

Frontend:

Flutter SDK

Emulador Android o Chrome (web).

4.3. Pasos para ejecutar el backend
# 1. Crear y activar entorno
python -m venv venv
venv\Scripts\activate  # en Windows

# 2. Instalar dependencias
pip install -r requirements.txt   # si lo creas
# o bien:
pip install flask flask_sqlalchemy werkzeug

# 3. Ejecutar API
python app.py

4.4. Pasos para exponer el backend con ngrok
ngrok http 5000

hay que copiar la URL de ngrok y pegarla en main.dart en ApiService.baseUrl
4.5. Pasos para ejecutar el frontend Flutter
flutter pub get
flutter run

4.6. Estructura de carpetas (resumen)
/
├── backend-flask/
│   ├── app.py
│   ├── uploads/
│   └── productos.db (no versionado o en .gitignore)
├── flutter_application_unab/
│   ├── lib/main.dart
│   ├── pubspec.yaml
│   └── android/ ...
└── README.md
