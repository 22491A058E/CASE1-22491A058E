import matplotlib.pyplot as plt
import numpy as np
import pandas as pd
anil=pd.read_csv('energy.csv')
print(anil)
#line chart
# andhra, karnataka
srh=anil[anil['State']=='Andhra']
rcb=anil[anil['State']=='Karnataka']

fig,diag=plt.subplots(2)
#date, consumption
diag[0].plot(srh['Date'],srh['Consumption'],color='red')
diag[1].plot(rcb['Date'],rcb['Consumption'],color='yellow')
revanth=anil[anil['State']=='Andhra']
cm=anil[anil['State']=='Karnataka']

fig,diag=plt.subplots(2)
#date, consumption
diag[0].bar(revanth['Date'],srh['Consumption'],color='red')
diag[1].bar(cm['Date'],rcb['Consumption'],color='yellow')

State1='Delhi'
State2='Odisha'
State3='Up'
State4='Punjab'
cse5=[State1,State2]
cse4=anil[anil['State']==State1]['Consumption'].sum()
cse3=anil[anil['State']==State2]['Consumption'].sum()

cse2=[cse3,cse4]

fig,diag=plt.subplots(2)
diag[0].pie(cse2,labels=cse5,autopct='%1.1f%%')
cse5=[State3,State4]
cse4=anil[anil['State']==State3]['Consumption'].sum()
cse3=anil[anil['State']==State4]['Consumption'].sum()

cse2=[cse3,cse4]

diag[1].pie(cse2,labels=cse5,autopct='%1.1f%%')
