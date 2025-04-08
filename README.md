# FarmTech Solutions - Modelagem de Banco de Dados

## Descrição do Projeto

Este projeto tem como objetivo criar um sistema de armazenamento e análise dos dados coletados pelos sensores utilizados em plantações para otimizar a irrigação e a aplicação de nutrientes. O modelo de banco de dados proposto é baseado no MER (Modelo Entidade-Relacionamento) e no DER (Diagrama Entidade-Relacionamento), e é capaz de armazenar dados históricos de sensores e ajustes feitos nas plantações.

## Entidades e Atributos

1. **Sensor**
   - `ID_Sensor`: Identificador único do sensor.
   - `Tipo`: Tipo de sensor (ex: "umidade", "pH", "nutriente").
   - `Data_Instalacao`: Data de instalação do sensor.

2. **Cultura**
   - `ID_Cultura`: Identificador único da cultura.
   - `Nome`: Nome da cultura (ex: "Soja", "Milho").
   - `Tipo_Cultivo`: Tipo de cultivo (ex: "irrigado", "não irrigado").

3. **Leitura**
   - `ID_Leitura`: Identificador único da leitura.
   - `Data_Hora`: Data e hora da leitura.
   - `Valor`: Valor da leitura do sensor.
   - `Tipo_Sensor`: Tipo de sensor utilizado na leitura.

4. **Ajuste**
   - `ID_Ajuste`: Identificador único do ajuste.
   - `Data_Hora`: Data e hora do ajuste.
   - `Tipo_Ajuste`: Tipo de ajuste feito (ex: "irrigação", "fertilização").
   - `Quantidade_Aplicada`: Quantidade de produto aplicado (ex: água ou fertilizante).

## Relacionamentos

1. **Sensor ↔ Leitura**: Um sensor pode ter muitas leituras. Relacionamento **1:N**.
2. **Cultura ↔ Leitura**: Uma cultura pode ter muitas leituras associadas. Relacionamento **1:N**.
3. **Leitura ↔ Ajuste**: Uma leitura pode gerar múltiplos ajustes. Relacionamento **1:N**.
