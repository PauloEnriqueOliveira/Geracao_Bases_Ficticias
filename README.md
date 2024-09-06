# Geração de Bases Ficticias

Esse repositório traz algumas maneiras de como você criar bases ficticias para estar usando em estudos, portifolios etc. Aqui você vai encontrar alguns exemplos que podem te ajudar. Qualquer dúvida, sinta-se à vontade para me chamar no [linkedin](https://www.linkedin.com/in/paulo-oliveira-a6650121a/).

## Descrição sobre cada file
- GBF - Este script tem como intuito fazer a geração de bases ficticias, nele vamos estar usando algumas bibliotecas como Faker que faz gerações de CPF's, Nomes brasileiros, cidades etc, para podermos estar usando em nossa base ficticia.
- Biblioteca [Faker](https://faker.readthedocs.io/en/master/locales/pt_BR.html).


#### - Geração de Nomes
~~~
nomes = [fake.name() for _ in range(num_rows)]
~~~

#### - Geração de Cidades
~~~
cidades = [fake.city() for _ in range(num_rows)]
~~~

#### - Geração de Telefones
~~~
telefones = [fake.phone_number() for _ in range(num_rows)]
~~~

#### - Geração de CPF's
~~~
cpfs = [fake.cpf() for _ in range(num_rows)]
~~~

#### - Geração de Valores
- Substitua o "x.x" pelos valores minimos e maximos.
~~~
def random_valor_real(min_val=x.x, max_val=x.x):
    return round(random.uniform(min_val, max_val), 2)

valores = [random_valor_real() for _ in range(num_rows)] 
~~~

#### - Geração de Booleans
~~~
boolean_column = np.random.choice([True, False], num_rows)
~~~

#### - Geração de Id's
- Substitua o "x" pelos valores minimos e maximos.
~~~
cod_pol = np.random.randint(x, x, num_rows)
~~~

#### - Geração de Data
- Substitua o "yyyy" - pelo ano, "mm" - pelo mês e "dd" - pelo dia.
~~~
from datetime import datetime, timedelta

def random_date(start, end):
    return start + timedelta(days=random.randint(0, (end - start).days))

start_date = datetime(yyyy, mm, dd)
end_date = datetime(yyyy, mm, dd)

date_insert = [random_date(start_date, end_date) for _ in range(num_rows)] 
~~~
