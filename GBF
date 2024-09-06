import pandas as pd
import numpy as np
from faker import Faker
import random
from datetime import datetime, timedelta

fake = Faker('pt_BR')

def random_date(start, end):
    return start + timedelta(days=random.randint(0, (end - start).days))

def random_valor_real(min_val=x.x, max_val=x.x):
    return round(random.uniform(min_val, max_val), 2)

num_rows = x linhas escolhidas 
start_date = datetime(yyyy, mm, dd)
end_date = datetime(yyyy, mm, dd)

nomes = [fake.name() for _ in range(num_rows)]
cidades = [fake.city() for _ in range(num_rows)] 
telefones = [fake.phone_number() for _ in range(num_rows)]  
valores = [random_valor_real() for _ in range(num_rows)]
cpfs = [fake.cpf() for _ in range(num_rows)] 
boolean_column = np.random.choice([True, False], num_rows) 
cod_pol = np.random.randint(x, x, num_rows) 
date_insert = [random_date(start_date, end_date) for _ in range(num_rows)] 

df = pd.DataFrame({
    'CPF': cpfs,
    'BOOLEAN': boolean_column,
    'COD. POL.': cod_pol,
    'DATA INSERT': date_insert,
    'Nome': nomes,
    'Cidade': cidades,
    'Telefone': telefones,
    'Valor (R$)': valores
})

df.to_csv('dados_ficticios.csv', sep=';', index=False)
