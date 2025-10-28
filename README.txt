INSTRUCCIONS D'ÚS
-----------------
Aquesta és una web local (prototip) per simular una cirurgia regenerativa de cap de fèmur i fèmur mitjançant bioimpressió 3D.

Com executar:
1. Descarrega el fitxer ZIP i descomprimeix-lo.
2. Obre el fitxer "index.html" amb un navegador modern (Chrome, Edge o Firefox). Si tens problemes amb la càrrega d'arxius STL a causa de polítiques de fitxers del navegador, executa amb un servidor local (opcional):
   - Python 3: `python -m http.server` dins la carpeta del projecte i obre http://localhost:8000
3. Carrega els fitxers STL amb els inputs "Subir STL".
4. Ajusta "Capas totales" i utilitza els controls per avançar/retrocedir o reproduir automàticament.
5. Canvia tipus de bio-tinta per veure el color aplicat a les capes.
6. Exporta anotacions o fa una instantània (snapshot).

Notes tècniques:
- El prototip utilitza Three.js des d'un CDN i STLLoader per parsejar fitxers .stl.
- Si no carregues STL, es mostra una geometria de demostració (cilindre + esfera).
- Per models grans, es recomana optimitzar l'STL (reduir polígons) per millorar el rendiment.


INSTRUCCIONS DE DESPLEGAMENT (VERCEL / NETLIFY) - CATALÀ


Per desplegar la web en línia (Vercel o Netlify) segueix aquests passos ràpids:

Opció A — Vercel (recomanat, gratuït per projectes petits):
1. Crea un compte a https://vercel.com i verifica'l.
2. Pugeu el projecte a un repositori de GitHub (carpeta amb index.html, styles.css i la carpeta models).
   - Per exemple:
     git init
     git add .
     git commit -m "Simulador bioimpressio"
     git branch -M main
     git remote add origin <URL_del_teu_repo>
     git push -u origin main
3. Al tauler de Vercel, fes clic a "New Project" → "Import Git Repository" → selecciona el repo.
4. Vercel detectarà un site estàtic (framework: Other). Accepta i desplega.
5. En uns segons tindràs una URL pública per compartir.

Opció B — Netlify:
1. Crea compte a https://app.netlify.com.
2. Pugeu el projecte a GitHub (com a l'opció A).
3. A Netlify, fes "New site from Git" i connecta el repo.
4. Configura el build command com buit i el directori de publicació com `/` (per sites estàtics simples).
5. Desplega i obtindràs una URL pública.

Executar localment (opció ràpida si no vols Git):
- Obre la carpeta i llança un servidor local:
  - Python 3: `python -m http.server`
  - Node (serve): `npx serve .`
- A continuació obre http://localhost:8000 al navegador.

OBSERVACIONS:
- Si utilitzes models STL grans, optimitza-los abans de pujar-los (reduir polígons).
- Mantingues la carpeta `models/` si vols que els exemples estiguin disponibles online.
