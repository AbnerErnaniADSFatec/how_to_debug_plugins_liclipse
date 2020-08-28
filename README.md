# Como debugar Python Plugins QGIS com o Liclipse

[![QGIS Software](https://img.shields.io/badge/QGIS%20Software-3.10.8-green)](https://qgis.org/en/site/)
[![Python Plugins QGIS](https://img.shields.io/badge/QGIS%20Plugins-latest-green)](https://plugins.qgis.org/)
[![Python QT](https://img.shields.io/badge/PyQt-5.15.0-green)](https://pypi.org/project/PyQt5/)
[![LiClipse](https://img.shields.io/badge/LiClipse-6.3.0-green)](https://www.liclipse.com/index.html)

A maneira mais eficaz para encontrar defeitos em um software é a partir de testes, porém alguns problemas correntes podem aparecer durante o desenvolvimento de software que podem ser facilmente identificados pelo processo de Debug. Como fazer debug no desenvolvimento de plugins no QGIS utilizando a IDE LiClipse utilizando Linux.

1. O primeiro passo é a instalação do LiClipse que pode ser baixado e instalado por este link https://www.liclipse.com/download.html;

2. Move the code to QGIS home plugins;

3. Open liclipse;

4. Open a linking repository from home QGIS;

5. Open window -> open perspective -> other;

6. Select Debug Perspective;

7. Select PyDev;

8. Select Start Debug Server;

9. Open QGIS;

10. Select QGIS settings;

11. Select "Use custom variables";

12. "Append" PYTHONPATH=/home/abner/liclipse/plugins/org.python.pydev.core_7.5.0.202001101115/pysrc/;

13. Go to QGIS Python Console:

```shell
>>> import pydevd
>>> pydevd.settrace(port=5678, suspend=False)
```

14. Create breakpoints;

15. Variables.
