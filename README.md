# Afterclass GitHub

## Error

Qué hacer cuando aparece el error: failed to push some refs to (repo url)

## Instrucciones

1. Creo mi repo remoto en GitHub (público, con archivos README y .gitignore)

2. En la terminal, inicializo Git en mi root con `git init`

3. Preparo el código para subirlo a GitHub con `git add .`

4. Pido a Git que lo administre con `git commit -m "subo repositorio local"`

5. Vinculo mi repo local con el remoto con `git remote add origin (repo url)`

6. Si mi rama local es master, le cambio el nombre con `git branch -M main`

7. Empujo mi repo local a GitHub con `git push -u origin main`

8. Me arroja el error porque no sabe identificar qué commit se realizó primero, si el local o remoto. Por lo que los combino con `git pull --rebase origin main`

9. Ahora mis commits van a estar secuenciados: va a aparecer primero el local y luego el remoto. Lo puedo comprobar con `git log`

10. Empujo finalmente mi repo local con `git push -u origin main`

## Aclaración

Una vez solucionado el error, cada vez que se realicen modificaciones localmente se deben utilizar los siguientes comandos:

1. Agrego todos los archivos modificados `git add .`

2. Pido a Git que lo administre con `git commit -m "modificación"`

10. Empujo a GitHub con `git push`