# Prediction of Grocery Store Sales Using Spatial Interaction Modelling (SIM)

This project is inspired by the Spatial Modelling for Retail Analytics course offered by the Consumer Data Research Center (CDRC) I recently attended. The course was held by Dr. Andy Newing and Dr. Nick Hood. Andy and Nick did a great job at introducing the class to sophisticated analysis and spatial modelling approaches that can be used to understand retail sector dynamics. Please check out all the CDRC courses and events here.
The technique that stood out the most to me was Spatial Interaction Modelling. This technique is used in social sciences to predict and describe behaviours that mimic gravitation interactions as described by Isaac Newton's law of gravity.

Three independent conditions are necessary for spatial interaction to occur:

* Complementarity: There must be supply and demand between the interacting locations. In the specific case of retailing, the supply side are the retail points, while the deman side is the available expenditure of customers.
* Intervening opportunity (lack of): Refers to a location that may offer a better alternative as a point of origin or as a point of destination. In retail for example, a customer visits a store becasue he/she must not have a closer store that offers similar array of goods.
* Transferability: Persons being transferred must be supported by transport infrastructures implying that origin and destination must be linked. the cost to overcome distance must not be higher than the benefits of the interaction.
Spatial interaction models seek to explain spatial flows between origins and destinations. In this example, the aim is to predict the flow of money into Sheffield grocery stores, given their location, and the available expenditure of the consumers in the modelled area.

The relationship between money flow, destinations and origins is given by the equation below:

Sij = Ai Oi Wj exp(−βCij)
 
Where,

Sij  = flow of expected flow of supermarket  j  from orgin  i 
Ai  = balancing factor that takes into account competition and ensures that demand is allocated to stores within the modelled region. it is calculated as:

Ai = 1 / ∑ Wj exp(−βCij)
 
Wj  = represents the overall attractiveness of store j. In this case size is used as a proxy of attractiveness.
exp(−βCij)  = represents the distance deterrence term.  β  is between 0 and 1.  β  = 0 means that the consumer does not mind travelling.  β = 1 means that the consumer does not want to travel.  Cij  represents the distance between origin and supermarket.
#### Important:
This analysis is an adaptation of Dr. Andy Newing's and Dr. Nick Hood's example projects at the CDRC course on Spacial Modelling for Retail Analytics. During the course the computations were made in Excel, I just applied the same models and ideas to a different dataset and modelled the analysis in Python.
