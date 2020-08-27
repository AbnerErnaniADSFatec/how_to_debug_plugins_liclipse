# Como debugar Python Plugins QGIS com o Liclipse



[![Python Plugins QGIS](https://img.shields.io/badge/QGIS%20Plugins-latest-green)](https://plugins.qgis.org/)
[![LeafLet](https://img.shields.io/badge/LiClipse-6.3.0-green)](https://www.liclipse.com/index.html)

Como fazer debug no desenvolvimento de plugins no QGIS utilizando a IDE Liclipse.

1. Install liclipse;

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
