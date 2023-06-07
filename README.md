# chmod+x on Windows

Windows no permite entregar permisos de ejecucion como ocurre con linux, por lo tanto si debemos versionar un script bash con permiso de ejecucion, debemos mediante git entregar el permiso de ejecucion.

```bash
# para agregar el permiso a un archivo aun no versionado
git update-index --add --chmod=+x hello.sh

# para agregar el permiso a un archivo existente en git
git update-index --chmod=+x hello.sh
```

Para probar que el permiso fue entregado correctamente, debemos ejecutar:

```bash
git status --porcelain=2
```

Estos cambios no son comiteados por github desktop, por lo que deben ser comiteados usando git bash:

```bash
git commit -m "add +x permision"
git push origin main
```
