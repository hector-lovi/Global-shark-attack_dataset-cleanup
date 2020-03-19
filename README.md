# Global Shark Attack Incidents
![jaws](https://i1.wp.com/codigoespagueti.com/wp-content/uploads/2015/06/jaws-6.jpg?fit=1080%2C608&quality=80&ssl=1)
## Intro
El objetivo de este proyecto es tomar decisiones sobre como limpiar los datos de [Global Shark Attack Incidents](https://www.kaggle.com/teajay/global-shark-attacks/version/1), un dataset alojado en la web de kaggle con registros sobre ataques de tiburones.

## Hipótesis
***¿Son los ataques de tiburones más usuales en hombres que en mujeres?***  
Como ya hemos comentado en la Intro, el objetivo del proyecto se basa en la limpieza de datos, sin embargo vamos a marcar un objetivo para poder tomar decisiones enfocadas a una misma dirección.

## Métodos
Los metodos que he utilizado para la limpieza de datos son:
- Visualización de los datos con `df.columns, df.describe() y df.dtypes`  
- Mapeado de datos nulos:  
```
cols = df.columns[:]
colours = ['#000099', '#ffff00'] # amarillo == valores nulos // azul == valores no nulos
sns.heatmap(df[cols].isnull(), cmap=sns.color_palette(colours))
```
