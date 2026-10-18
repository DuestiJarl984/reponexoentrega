# Publicación en GitHub — instrucciones rápidas

1. Inicia sesión en GitHub y crea un repositorio vacío, por ejemplo `NexoEntrega360` (sin README automático).
2. En una terminal, entra a la carpeta `NexoEntrega360`.
3. Si recibiste el ZIP, inicializa el repositorio y crea un commit real:

   ```bash
   git init
   git add .
   git -c user.name="Nombre de la persona que sube" -c user.email="su-correo@example.com" commit -m "Entrega NexoEntrega360"
   git branch -M main
   git remote add origin https://github.com/USUARIO/NexoEntrega360.git
   git push -u origin main
   ```

4. Abre la pestaña **Actions**, entra a `pruebas-nexo` y confirma si la ejecución es verde. Si falla, corrige y vuelve a subir.
5. Ejecuta `git rev-parse HEAD` y pega el resultado exacto en el PDF, junto con el enlace al repositorio y al workflow.
6. Entrega a través del aula el mismo PDF para las cinco personas.

**Nota:** no uses `USUARIO` literalmente: reemplázalo por la cuenta/organización de GitHub que realmente abrió el repositorio. No afirmes que Actions pasó hasta verlo.
