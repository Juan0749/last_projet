# Control de Pacientes

Abrir `index.html` en el navegador para registrar pacientes, tratamientos, abonos y alertas de deuda tras 10 días.

## Instalar `xmllint`

`xmllint` viene dentro del paquete **libxml2** (o `libxml2-utils` según distro). Ejemplos:

- Ubuntu / Debian:
  - `sudo apt update && sudo apt install -y libxml2-utils`
- Fedora / RHEL / CentOS:
  - `sudo dnf install -y libxml2`
- Alpine:
  - `sudo apk add libxml2-utils`
- macOS (Homebrew):
  - `brew install libxml2`
  - opcional para dejarlo en PATH:
    - `echo 'export PATH="$(brew --prefix libxml2)/bin:$PATH"' >> ~/.zshrc`

Verificar:

- `xmllint --version`
