## Expensas On-Line Predictive API

This project is a simple API to predict if the Expensas On-line users will pay on time the next month.


## Requirements

1. Python3
2. Pip3
3. Virtualenv

## Set up

1. Clone this repo
2. Create a virtualenv for this project
3. Activate the virtualenv. Be sure to create the virtualenv wiht python3. To do that, you can use the -p option. `virtualenv -p path/to/python3 virtualenvname`
4. Install the requirements `pip3 install -r requirements.txt`
5. Configure the port where you want the server runs in the config.json file
5. Once all the requirements are satisfied, you have just to run the server executing `python3 apy.py`. **IMPORTANT** you must execute the aforementioned command from the scr folder.

## Use

To get the models prediction you have to make a POST with the following structure
```
{
	"unidades": [
		{
			"unidad_id":int,
			"unidad_tipo": string,
			"expensa_mes": int,
			"pago_metodo_lag_1": string,
			"pago_metodo_lag_2": string,
			"pago_metodo_lag_3": string,
			"pago_metodo_lag_4": string,
			"pago_metodo_lag_5": string,
			"pago_metodo_lag_6": string
		
		}
	]
}
```

For example:
```
{
	"unidades": [
		{
			"unidad_id":500,
			"unidad_tipo": "Departamento",
			"expensa_mes":12,
			"pago_metodo_lag_1": "Débito directo",
			"pago_metodo_lag_2": "Impago",
			"pago_metodo_lag_3": "Impago",
			"pago_metodo_lag_4": "Impago",
			"pago_metodo_lag_5": "Impago",
			"pago_metodo_lag_6": "Impago"
		
		}
	]
}
```




