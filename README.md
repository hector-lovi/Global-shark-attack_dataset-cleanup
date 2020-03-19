# Global Shark Attack Incidents
![jaws](https://i1.wp.com/codigoespagueti.com/wp-content/uploads/2015/06/jaws-6.jpg?fit=1080%2C608&quality=80&ssl=1)
## Intro
El objetivo de este proyecto es tomar decisiones sobre como limpiar los datos de [Global Shark Attack Incidents](https://www.kaggle.com/teajay/global-shark-attacks/version/1), un dataset alojado en la web de kaggle con registros sobre ataques de tiburones.

## Hipótesis
***¿Son los ataques de tiburones más usuales en hombres que en mujeres?***  
Como ya hemos comentado en la Intro, el objetivo del proyecto se basa en la limpieza de datos, sin embargo vamos a marcar un objetivo para poder tomar decisiones enfocadas a una misma dirección.

## Métodos
Los metodos que he utilizado para la limpieza de datos son:  
- Lectura de ficheros y creación de DataFrames (Pandas).
- Visual de los datos en crudo con `df.columns, df.describe() y df.dtypes`.  
- Mapeado de datos nulos:  
```
cols = df.columns[:]
colours = ['#000099', '#ffff00'] # amarillo == valores nulos // azul == valores no nulos
sns.heatmap(df[cols].isnull(), cmap=sns.color_palette(colours))
```  
- Transformación de columnas a través de funciones.  
- Dropeo de columnas.  
- Regex.  
- Plots con matplotlib.  
- Volcado de datos en csv.  

## Conclusiones
Existe todo un universo de posibilidades en cuanto a limpieza de datos se refiere, y muchas librerias que pueden hacernos la vida muy facil, sin embargo destacaría **Pandas** por encima del resto.  

En cuanto al trato de resultados nulos, no existen parametros fijos sobre como debemos manipular dichos datos. La forma mas eficiente es hacer una valoración en función del objetivo que queramos alcanzar.

