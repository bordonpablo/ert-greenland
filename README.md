# ERT Greenland - pyGIMLi

El objetivo del proyecto es adaptar los datos de salida del equipo ??? a la estructura de datos esperada por la libreria [pyGIMLi](https://www.pygimli.org/index.html) para realizar inversiones de **Electrical Resistivity Tomography**.

El proceso de [instalacion](https://www.pygimli.org/installation.html) de la libreria es via conda.

## Ejemplo 1: ERT field data with topography

### Referencias

* Documentacion: [plot_02_ert_field_data.html](https://www.pygimli.org/_examples_auto/3_ert/plot_02_ert_field_data.html)
* Script: [plot_01_ert_2d_mod_inv.py](https://github.com/gimli-org/pyGIMLi/blob/main/doc/examples/3_ert/plot_01_ert_2d_mod_inv.py)
* Data: [slagdump.ohm](https://github.com/gimli-org/example-data/blob/master/ert/slagdump.ohm)

### Estrategia

* Levantar el archivo nuestro.
* Crear **DataContainerERT** vacio (estructura de datos utilizada internamente)
* Llenar la estructura con nuestra data
* Inventar informacion contextual faltante de ser necesario
* Continuar procesamiento normal

### API involucrada

```python
import matplotlib.pyplot as plt
import pygimli as pg
from pygimli.physics import ert
```

* Clase raiz modulo (**"import pygimli as pg"**)
  * [pagina inicial](https://www.pygimli.org/gimliapi/namespaceGIMLI.html)
  * [metodo z()](https://www.pygimli.org/gimliapi/namespaceGIMLI.html#a28ff682d3fff73dd462040c5cb8ee981)
* Clase ERT (**"from pygimli.physics import ert"**)
  * [Pagina inicial](https://www.pygimli.org/pygimliapi/_generated/pygimli.physics.ert.html#module-pygimli.physics.ert)
  * [metodo createGeometricFactors()](https://www.pygimli.org/pygimliapi/_generated/pygimli.physics.ert.html#pygimli.physics.ert.createGeometricFactors)
* DataContainerERT
  * [Documentacion](https://www.pygimli.org/_tutorials_auto/0_basics/plot_3-data_container.html)
  * [Pagina inicial](https://www.pygimli.org/gimliapi/classGIMLI_1_1DataContainerERT.html)
  * [ancestro](https://www.pygimli.org/gimliapi/classGIMLI_1_1DataContainer.html)
  * [otra pagina](https://www.pygimli.org/pygimliapi/_generated/pygimli.physics.ert.html#pygimli.physics.ert.DataContainer)
