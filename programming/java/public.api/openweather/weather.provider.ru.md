# Суть примера - реализовать логику получения данных с внешнего портала API.
> В данном примере будет применена урезанная логика SPI шаблона (Serive Provider Interface). Рекомендуется погуглить на эту тему так как следующий пример будет тесно с этим связан. А в текущем примере будет рассмотрен упрощенный вариант SPI.

* Суть сводиться к тому что нам необходимо создать "интерфейс" для облегчения получения инфы с удаленного ресурса.
* В качестве поставщика данных будет использован openweathermap.org. Но кому будет интересно, вот еще [список](https://github.com/public-apis/public-apis) разных доступных провайдеров.

* ПЕРВЫЙ ЭТАП, необходимо [создать аккаунт](https://home.openweathermap.org/users/sign_up) на openweathermap в процессе вы получите доступ к авторизационному ключу.
* Обмен данными с этим API будет происходить через по http(s)
* При этом если обратить внимание на их API, в нем есть очень много "endpoints" адрессов или страниц, каждая из которых выдает определенный тип информации
* Так же обратите внимание что для того чтобы передавать настройки (фильтра) в URL вбивают,парами "параметры": напр units=metric переведем единицы измерения в метрические, или city=Chisinau, выдаст инфу для указанного города
* Между параметрами URL вставляются "&"-ы а первый параметр всегда после адреса "endpoint" вставляется через "?"
* Так что, например - если бы нам захотелось получить текущую погоду **api.openweathermap.org/data/2.5/weather** для Кишинева +**?city=Chisinau** в метрических единицах  +**&units=metric**  То нам бы пришлось отправить запрос (или считывать) с адреса "https://api.openweathermap.org/data/2.5/weather?city=Chisinau&units=metric"
* Документация [тут](https://openweathermap.org/api)
* Полученные данные распарсить в виде JSON при помощи https://mvnrepository.com/artifact/org.json/json
---
Требуется выполнить следующее:
1.  Создать класс "OpenWeatherProvider" вот стартер код:

```java
public class OpenWeatherProvider {
	
	/**
	 * endpoint: api.openweathermap.org/data/2.5/weather
	 * params: city, units
	 * */
	public Float  getCurrentTemperature(String city) {
		
	}
	
	
	/**
	 * endpoint: api.openweathermap.org/data/2.5/forecast/daily
	 * params: city, units
	 * */	
	public ArrayList<Float>  getForecast16DaysTemperature(String city) {
		
	}	
	
}

```

2. Укомплектовать код методов таким образом чтобы getCurrentTemperature вернул текушую температуру для желаемого города в градусах Celsius, а getForecast16DaysTemperature вернул Список прогнозируемых температур для следующих 16 дней для желаемого города в градусах Celsius.

---
БОНУС - после реализации методов, улучшить код класс провайдера.

