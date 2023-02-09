Introdução
****

01.O que é chatGPT3
=====

.. image:: CONCATENACAO.png
   :align: center
   :width: 650

•	**Concatenar é** o nome da técnica de empilhar um *Data Frame* sobre outro. Ou seja, **juntar dois *Data Frames*.**
•	Imagine que queremos concatenar (juntar) os dois *Data Frames* de vendas, tanto das franquias do estado de SP como de MG. Para isso, usamos o método **``concat( )``** com os seus parâmetros:
  •	**Lista de *Data Frames* na ordem a serem agrupados:
    •	Exemplo: **``[df.vendas_sp, df_vendas_mg]``**
  •	**``ignore_index``**: gera novos índices para o novo *Data Frame*.
  
.. code-block:: python
   :linenos:
   
    # CONCATENANDO DOIS DATAFRAMES
    df_vendas_totais = pd.concat([df_vendas_sp,df_vendas_mg], 
                                  ignore_index=True)
                                  
    # VISUALIZANDO O NOVO DATAFRAME df_vendas_totais
    df_vendas_totais.head(15)
    
 .. image:: VENDAS_FRANQUIAS.png
   :align: center
   :width: 400
