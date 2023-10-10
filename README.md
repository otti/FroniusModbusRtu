# Communication between Fronius Symo GEN24 10.0 Plus and Fronius Smart meter TS 65A-3

Every value is stored in two registers with 16 bit each. These two registers will be combined to one 32 bit value.
The low word is stored at the lower address.
This 32 bit value will be interpreded as singned 32 bit integer.

## Read holding register for device ID 1 , Start address = 258 Quantity = 16
Every second  
<table>
   <tr>
      <th>Reg</td>
      <th>Description</td>
      <th>Unit</td>
   <tr>
   <tr>
      <td>258..259</td>
      <td>Voltage</td>
      <td>0.1 V</td>
   </tr>
   <tr>
      <td>260..261</td>
      <td>Voltage Phase Phase</td>
      <td>0.1 V</td>
   </tr>
   <tr>
      <td>262..263</td>
      <td>PowerReal_P_Sum OR PowerFactor_Sum OR Current_AC_Sum???</td>
      <td></td>
   </tr>
   <tr>
      <td>264..265</td>
      <td>PowerApparent_S_Sum</td>
      <td>0.1 VA</td>
   </tr>
   <tr>
      <td>266..267</td>
      <td>PowerReactive_Q_Sum</td>
      <td>0.1 var</td>
   </tr>
   <tr>
      <td>268..269</td>
      <td>PowerReal_P_Sum OR PowerFactor_Sum OR Current_AC_Sum???</td>
      <td></td>
   </tr>
   <tr>
      <td>270..271</td>
      <td>PowerReal_P_Sum OR PowerFactor_Sum OR Current_AC_Sum???</td>
      <td></td>
   </tr>
   <tr>
      <td>272..273</td>
      <td>Frequency</td>
      <td>0.1 Hz</td>
   </tr>
</table>
  
  

## Read holding register for device ID 1 , Start address = 286 Quantity = 42
Every second  

<table>
   <tr>
      <th>Reg</td>
      <th>Description</td>
      <th>Unit</td>
   <tr>
   <!--- Phase 1 -->
   <tr>
      <td colspan="3"><b>Phase 1</b></td>
   </tr>
   <tr>
      <td>286..287</td>
      <td>Voltage_AC_PhaseToPhase_12</td>
      <td>0.1 V</td>
   </tr>
   <tr>
      <td>288..289</td>
      <td>Voltage_AC_Phase_1</td>
      <td>0.1 V</td>
   </tr>
   <tr>
      <td>290..291</td>
      <td>Current_AC_Phase_1</td>
      <td>mA</td>
   </tr>
   <tr>
      <td>292..293</td>
      <td>PowerReal_P_Phase_1</td>
      <td>0.1 W</td>
   </tr>
   <tr>
      <td>294..295</td>
      <td>PowerApparent_S_Phase_1</td>
      <td>0.1 VA</td>
   </tr>
   <tr>
      <td>296..297</td>
      <td>PowerReactive_Q_Phase_1</td>
      <td>0.1 var</td>
   </tr>
   <tr>
      <td>298..299</td>
      <td>PowerFactor_Phase_1</td>
      <td>0.001</td>
   </tr>
   <!--- Phase 2 -->
   <tr>
      <td colspan="3"><b>Phase 2</b></td>
   </tr>
   <tr>
      <td>300..301</td>
      <td>Voltage_AC_PhaseToPhase_23</td>
      <td>0.1 V</td>
   </tr>
   <tr>
      <td>302..303</td>
      <td>Voltage_AC_Phase_2</td>
      <td>0.1 V</td>
   </tr>
   <tr>
      <td>304..305</td>
      <td>Current_AC_Phase_2</td>
      <td>mA</td>
   </tr>
   <tr>
      <td>306..307</td>
      <td>PowerReal_P_Phase_2</td>
      <td>0.1 W</td>
   </tr>
   <tr>
      <td>308..309</td>
      <td>PowerApparent_S_Phase_2</td>
      <td>0.1 VA</td>
   </tr>
   <tr>
      <td>310..311</td>
      <td>PowerReactive_Q_Phase_2</td>
      <td>0.1 var</td>
   </tr>
   <tr>
      <td>312..313</td>
      <td>PowerFactor_Phase_2</td>
      <td>0.001</td>
   </tr>
   <!--- Phase 3 -->
   <tr>
      <td colspan="3"><b>Phase 3</b></td>
   </tr>
   <tr>
      <td>314..315</td>
      <td>Voltage_AC_PhaseToPhase_31</td>
      <td>0.1 V</td>
   </tr>
   <tr>
      <td>316..317</td>
      <td>Voltage_AC_Phase_3</td>
      <td>0.1 V</td>
   </tr>
   <tr>
      <td>318..319</td>
      <td>Current_AC_Phase_3</td>
      <td>mA</td>
   </tr>
   <tr>
      <td>320..321</td>
      <td>PowerReal_P_Phase_3</td>
      <td>0.1 W</td>
   </tr>
   <tr>
      <td>322..323</td>
      <td>PowerApparent_S_Phase_3</td>
      <td>0.1 VA</td>
   </tr>
   <tr>
      <td>324..325</td>
      <td>PowerReactive_Q_Phase_3</td>
      <td>0.1 var</td>
   </tr>
   <tr>
      <td>326..327</td>
      <td>PowerFactor_Phase_3</td>
      <td>0.001</td>
   </tr>
</table>

## Read holding register for device ID 1 , Start address = 1024 Quantity = 16
Every 10 seconds  

Every energy value is stored in four registers.  
Example for EnergyReactive_VArAC_Sum_Produced:  
For example the actual energy value is 463941 Wh. The kilowatt hours (463) are stored in register 1036..1037. The watt hours (941) are stored in register 1038..1039. 
To get the total energy in Wh multiply register 1036..1037 by 1000 and add register 1038..1039 to it.

<table>
   <tr>
      <th>Reg</td>
      <th>Description</td>
      <th>Unit</td>
   <tr>
   <tr>
      <td>1024..1025</td>
      <td>EnergyReal_WAC_Plus_Absolute,  EnergyReal_WAC_Sum_Consumed</td>
      <td>kWh</td>
   </tr>
   <tr>
      <td>1026..1027</td>
      <td>EnergyReal_WAC_Plus_Absolute,  EnergyReal_WAC_Sum_Consumed</td>
      <td>Wh</td>
   </tr>
   <tr>
      <td>1028..1029</td>
      <td>EnergyReactive_VArAC_Sum_Consumed</td>
      <td>kvarh</td>
   </tr>
   <tr>
      <td>1030..1031</td>
      <td>EnergyReactive_VArAC_Sum_Consumed</td>
      <td>varh</td>
   </tr>
   <tr>
      <td>1032..1033</td>
      <td>EnergyReal_WAC_Minus_Absolute, EnergyReal_WAC_Sum_Produced </td>
      <td>kWh</td>
   </tr>
   <tr>
      <td>1034..1035</td>
      <td>EnergyReal_WAC_Minus_Absolute, EnergyReal_WAC_Sum_Produced </td>
      <td>Wh</td>
   </tr>
   <tr>
      <td>1036..1037</td>
      <td>EnergyReactive_VArAC_Sum_Produced</td>
      <td>kvarh</td>
   </tr>
   <tr>
      <td>1038..1039</td>
      <td>EnergyReactive_VArAC_Sum_Produced</td>
      <td>varh</td>
   </tr>
</table>

## Test conditions

### Inverter
Fronius Symo GEN24 10.0 Plus  
SW: 1.19.7-1 on 2023-02-28  

### Smart Meter
Fronius TS 65A-3

