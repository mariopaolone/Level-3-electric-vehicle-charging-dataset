# Level-3-electric-vehicle-charging-dataset
Level 3 electric vehicle charging dataset made available by the EPFL Distributed Electrical Systems Laboratory

Description of the commercial EV charging station used to collect the dataset
The dataset has been collected on a level 3 electric vehicle (EV) charging station located in south western Switzerland. The data has been measured from April 12th 2022 to July 4th 2023.
The charging station includes 6 charging plugs: 2xCCS, 1xCHAdeMO, 1xType 2 socket, 1xType 2 plug, and 1xTesla DC. Only measurements from the CCS plugs are included in the dataset as the utilization of other charging options were significantly lower. The maximum power of the charging station is 172.5 kW and two EVs can be supplied at the same time. 
In case of two simultaneous charging sessions, the power capacity is equally divided however, in case one EV draws less power than the allocated one by the charging station, the otherwise unused capacity is allocated to the other EV.
The data is retrieved by a custom-made data acquisition software developed by the EPFL-DESL. The data include measurement and session data. The measurement dataset consist of 64277 measurements with a 1-minute resolution. The session dataset consists of 1878 EV charging sessions contained in the measurement data. The description of the two dataset is reported here below.<br>

Measurement dataset<br>
A measurement data point includes the following values:<br> 
•	Data and time<br>
•	CCS                 Plug ID (CCS1 or CCS2)<br>
•	Session	ID          number attributed to the charging session<br>
•	P                   AC charging power of the charging station [W]<br>
•	Pset                Power setpoint set by the charging station [W]<br>
•	Preq		            Power requested by the EV [W]<br>
•	TotalCapacity	      Total energy capacity of the EV’s battery [a-dimensional]<br>
•	RemainingCapacity	  Remaining energy in the EV’s battery [a-dimensional]<br>
•	BulkCapacity	      Usable energy capacity of the EV’s battery [a-dimensional]<br>
•	Energy	            Cumulative energy charged of the charging session [Wh]<br>
•	SOC		              State-of-charge of the EV’s battery [%]<br>
•	Ctrl_t		          Boolean identifying whether Pset < Preq at the time interval (0=False,1=True)<br>
•	Ctrl_s		          Boolean identifying whether Pset < Preq anytime during the charging session (0=False, 1=True)<br>

Quantities are recorded with a sampling time of one minute.<br>

Session dataset<br>
Each charging session includes the following values:<br>
•	Session	ID          number attributed to the charging session<br>
•	CCS		              Plug ID (CCS1 or CCS2)<br>
•	Arrival	            EV arrival time<br>
•	Departure	          EV departure time<br>
•	Stay 		            EV stay duration [min]<br>
•	Energy 	            Charged energy [Wh]<br>
•	Pmax		            Maximum AC charging power of the session [W]<br>
•	Preq_max	          Maximum requested power of the session [W]<br>
•	Controlled session 	Boolean identifying whether Pset < Preq anytime during the charging session (0=False, 1=True)<br>
•	TotalCapacity	      Total energy capacity of the EV’s battery [a-dimensional]<br>
•	BulkCapacity	      Usable energy capacity of the EV’s battery [a-dimensional]<br>
•	SOC arrival	        State-of-charge of the EV’s battery at arrival [%]<br>
•	SOC departure	      State-of-charge of the EV’s battery at departure [%]<br>
•	Energy capacity 	  Approximated capacity of the EV’s battery [Wh]<br>
