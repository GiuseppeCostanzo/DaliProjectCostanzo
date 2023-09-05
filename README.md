Giuseppe Costanzo
# Progetto DALI: Servizi Bancari
Referenze : https://github.com/AAAI-DISIM-UnivAQ/DALI

## Descrizione

L’idea del progetto è quella di simulare un ambiente, in particolare un servizio bancario (o postale) dove poter effettuare le classiche operazioni.
In tale dominio vi sono 3 tipologie di agenti : cliente, sportellista e ticket (il bigliettaio).
Quando un cliente arriva in banca per effettuare una operazione, si reca prima dal ticket per richiedere un biglietto (un numero intero progressivo), che servirà allo sportellista per gestire la clientela. L’agente ticket rilascia dunque tale progressivo al cliente (che parte da 1 e aumenta man mano che arrivano clienti), e il cliente attenderà dunque il suo turno.
Nel mentre, l’agente ticket notifica l’agente sportellista che vi sono nuovi clienti in coda da servire. Lo sportellista dunque, se libero, chiamerà il primo cliente utile (ossia quello avente progressivo più piccolo). A questo punto il cliente che viene chiamato si reca dallo sportellista, e può effettuare tre tipologie di operazione dal proprio conto corrente: pagamento, deposito (versamento), e prelievo. Tali operazioni non sono deterministiche, ma sono scelte dall’agente in modo casuale
Il cliente, una volta scelta la tipologia di operazione, specifica l’importo, e nel caso di pagamento e prelievo, se sceglie un valore maggiore di ciò che ha nel proprio conto corrente l’operazione verrà negata.
Nella specifica implementazione, vi sono un agente sportellista, un agente ticket, e 3 agenti clienti. Si noti che questo sistema di gestione della clientela può potenzialmente gestire n clienti


