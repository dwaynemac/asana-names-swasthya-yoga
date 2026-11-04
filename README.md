# Ásanas — Swásthya Yôga

Skill de nomenclatura de ásanas de Swásthya Yôga para consultar las referencias del repositorio antes de nombrar, describir, traducir o comparar posturas, conservando su grafía, acentos y variantes.

## Instalación

La skill **asana-names-swasthya-yoga** incluye las instrucciones y las referencias de nomenclatura. Elegí la instalación según el agente que uses.

### Codex, Claude Code y otros agentes locales: con `npx skills`

Con Node.js 22.20 o posterior, ejecutá este comando desde la carpeta de tu proyecto:

```sh
npx skills add dwaynemac/asana-names-swasthya-yoga --skill asana-names-swasthya-yoga
```

Seguí las indicaciones para elegir el agente y confirmar la instalación. El comando descarga la skill con sus referencias; no necesitás preparar un ZIP ni descargar el repositorio manualmente. Para tenerla disponible en todos tus proyectos, agregá `-g` al comando.

Esta opción instala archivos para agentes locales. Para usarla en ChatGPT web o Claude web, seguí las instrucciones de carga o de skills compartidas de abajo. Consultá la [documentación de `skills`](https://github.com/vercel-labs/skills#install-a-skill).

### ChatGPT y Claude web: con un ZIP o una skill compartida

Si alguien de tu espacio de trabajo ya la compartió con vos, podés instalarla o habilitarla desde la lista de skills compartidas, sin descargar archivos. Para cargarla por tu cuenta, pedile a quien la distribuye el archivo **asana-names-swasthya-yoga.zip** listo para subir. No necesitás descargar el repositorio ni usar una terminal.

### ChatGPT

1. En la barra lateral, abrí **Plugins** y seleccioná la pestaña **Skills**.
2. Seleccioná **Create → Upload from your computer**.
3. Cargá `asana-names-swasthya-yoga.zip` y esperá a que termine la revisión.
4. Comprobá que la skill esté instalada y disponible para usar.

Si ya te la compartieron, buscala en **Skills → Shared with me** o **Shared by {nombre del espacio de trabajo}** y seleccioná **••• → Install**.

La función está disponible para cuentas elegibles de Business, Enterprise, Healthcare y Edu, según la configuración del espacio de trabajo. Consultá la [guía oficial de skills en ChatGPT](https://help.openai.com/en/articles/20001066-skills-in-chatgpt/).

### Claude

1. Abrí **Customize → Skills**.
2. Seleccioná **+ → Create skill → Upload a skill**.
3. Cargá `asana-names-swasthya-yoga.zip`.
4. Comprobá que la skill aparezca habilitada en la lista.

Si ya te la compartieron dentro de tu organización, habilitala desde tu lista de skills.

Necesitás tener habilitada la ejecución de código y creación de archivos. En cuentas de organización también depende de sus permisos. Consultá [cómo usar skills en Claude](https://support.claude.com/en/articles/12512180-use-skills-in-claude).

<details>
<summary>Para quien distribuye la skill: preparar el ZIP</summary>

Este repositorio todavía no ofrece un ZIP listo para descargar. Para prepararlo, ejecutá lo siguiente desde la carpeta del repositorio:

```sh
cd skills
zip -r ../asana-names-swasthya-yoga.zip asana-names-swasthya-yoga
```

El archivo debe contener la carpeta `asana-names-swasthya-yoga` con su `SKILL.md` y las referencias incluidas. Distribuí ese ZIP a quienes quieran cargar la skill; compartir solamente `SKILL.md` deja afuera las fuentes de nomenclatura.

</details>

## Uso

Con la skill disponible en tu agente, podés invocarla explícitamente:

```text
Usá la skill asana-names-swasthya-yoga para revisar los nombres de ásanas
de esta secuencia según las referencias de Swásthya Yôga.
```

También está configurada para activarse implícitamente cuando una respuesta incluya nombres de ásanas, si el agente admite esa función. Se aplica a clases, secuencias, contenido docente y otras consultas que mencionen estas posturas; no cambia los nombres de ejercicios ajenos a los ásanas.

La skill busca cada nombre en el índice de nomenclatura y consulta las familias, variantes y correlaciones extraídas de `asanas-tratado.pdf`. Cuando un nombre no puede verificarse, describe la postura y señala la incertidumbre, sin inventar equivalencias entre escuelas.

## Contenido

| Archivo | Propósito |
| --- | --- |
| [plugin.json](plugin.json) | Manifiesto general del plugin. |
| [.codex-plugin/plugin.json](.codex-plugin/plugin.json) | Manifiesto para Codex y ubicación de las skills. |
| [SKILL.md](skills/asana-names-swasthya-yoga/SKILL.md) | Instrucciones de verificación y uso de la nomenclatura. |
| [agents/openai.yaml](skills/asana-names-swasthya-yoga/agents/openai.yaml) | Configuración de interfaz e invocación de la skill. |
| [nomenclatura.md](skills/asana-names-swasthya-yoga/references/nomenclatura.md) | Índice alfabético de nombres del PDF, con familia y números de variante. |
| [familias.md](skills/asana-names-swasthya-yoga/references/familias.md) | Índice de las 123 familias y detalle desde la 3, con nombres de variantes, números originales y correlaciones del PDF. |
| [correlaciones.md](skills/asana-names-swasthya-yoga/references/correlaciones.md) | Correlaciones aportadas por el usuario, separadas de las del PDF. |

Las referencias están incluidas como texto Markdown; no hace falta volver a aportar el PDF para consultarlas. Contienen únicamente nombres, números y correlaciones, sin categorías, niveles, notas ni imágenes. Este repositorio contiene instrucciones y documentación, sin una aplicación que compilar ni dependencias de ejecución propias.

## Alcance de las referencias

- Conservar la grafía documentada y los calificadores de cada variante.
- Conservar la numeración original de las 2121 variantes numeradas. Las celdas vacías corresponden a nombres sin número en el PDF.
- Las familias 1 y 2 aparecen únicamente en el índice general; el detalle empieza en la familia 3.
- Distinguir las correlaciones del PDF de las aportadas por el usuario.
- Citar la referencia, la familia y el número de técnica, cuando corresponda, si se solicita una fuente o es necesario justificar una distinción.
- Las correlaciones de nombres no confirman por sí solas que la ejecución sea idéntica.
- La nomenclatura es una convención terminológica y no establece indicaciones terapéuticas ni la seguridad de una práctica.
