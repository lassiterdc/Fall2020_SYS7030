# Fall2020_SYS7030
Created 9/11/2020

SYS 7030 Project - Concept Note

Context: There are 7 reservoirs in the Columbia River Basin which serve many purposes including hydropower production, irrigation water supply, and drinking water supply with other operating objectives such as facilitating fish migrations and mitigating flood risks.

Problem: Current operation policies (i.e. patterns of retention and release) may not optimize for the objectives and may not be readily adaptable to changing watershed conditions like climate, land use, and policy changes. My classmate is attempting to deploy a deterministic optimization approach assuming perfect information to find optimal operations during the historical record and compare those results to stochastic optimization models to judge performance. Another teammate is going to help by using concepts from information theory to identify the most valuable variables and lags to condition the stochastic optimization model. The model will probably be optimized at a daily time step since variables like electricity demand are more volatile, but more coarse resolution information may be valuable for constraining the optimization problem as well. One of the more coarse sources of information potentially useful for constraining the optimization are 'naturalized' monthly inflows to each reservoir which is where my project comes in.

My Goal: Develop monthly naturalized flow forecasts for each reservoir to be used for conditioning the stochastic optimization of reservoir operations.

Method: Build a multivariate time series model ensemble of naturalized monthly inflows at each reservoir (i.e. flows that would be there in the absence of human intervention). Each model will output a sum of flows for all modeled reservoirs for a 3 month period which will be disaggregated into monthly flows at each gage using stochastic modeling techniques. The ensemble models will include various combinations of predictor variables at different time lags. 

Data: Naturalized flows, geopotential height, meriodonal winds, zonal winds, sea surface termperature, snow-water equivalent, and PDSI data.

