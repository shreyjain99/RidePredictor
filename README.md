<h2 align= "center"><em>Ride Predictor (NYC city)</em></h2>

<div align="center">
  <img height="400" src="https://github.com/shreyjain99/RidePredictor/blob/main/src%20files/New_york.gif"/>
</div>

<hr width="100%" size="2">

<h4 align= "left"> <b> About Project (Data and Problem formulation) </b> </h4>

<br>

<p>
<strong>Get the data from :</strong> http://www.nyc.gov/html/tlc/html/about/trip_record_data.shtml
The data used in the attached datasets were collected and provided to the NYC Taxi and Limousine Commission (TLC) 
</p>

<br>

<p>
<strong>Data Collection :</strong>
We Have collected all yellow taxi trips data of jan-2015 to mar-2015 and jan-2016 to mar-2016
</p>
<table>
<tr>
<th> file name </th>
<th> file name size</th>
<th> number of records </th>
<th> number of features </th>
</tr>
<tr>
<td> yellow_tripdata_2016-01 </td>
<td> 1. 59G </td>
<td> 10906858 </td>
<td> 19 </td>
</tr>
<tr>
<td> yellow_tripdata_2016-02 </td>
<td> 1. 66G </td>
<td> 11382049 </td>
<td> 19 </td>
</tr>
<tr>
<td> yellow_tripdata_2016-03 </td>
<td> 1. 78G </td>
<td> 12210952 </td>
<td> 19 </td>
</tr>
<tr>
<td> yellow_tripdata_2015-01 </td>
<td> 1.84Gb </td>
<td> 12748986 </td>
<td> 19 </td>
</tr>
<tr>
<td> yellow_tripdata_2015-02 </td>
<td> 1.81Gb </td>
<td> 12450521 </td>
<td> 19 </td>
</tr>
<tr>
<td> yellow_tripdata_2015-03 </td>
<td> 1.94Gb </td>
<td> 13351609 </td>
<td> 19 </td>
</tr>
</table>

<br>

<p>
<strong>Features in the dataset :</strong>
</p>
<table border="1">
    <tr>
        <th>Field Name</th>
        <th>Description</th>
    </tr>
    <tr>
        <td>VendorID</td>
        <td>
            A code indicating the TPEP provider that provided the record.
            <ol>
                <li>Creative Mobile Technologies</li>
                <li>VeriFone Inc.</li>
            </ol>
        </td>
    </tr>
    <tr>
        <td>tpep_pickup_datetime</td>
        <td>The date and time when the meter was engaged.</td>
    </tr>
    <tr>
        <td>tpep_dropoff_datetime</td>
        <td>The date and time when the meter was disengaged.</td>
    </tr>
    <tr>
        <td>Passenger_count</td>
        <td>The number of passengers in the vehicle. This is a driver-entered value.</td>
    </tr>
    <tr>
        <td>Trip_distance</td>
        <td>The elapsed trip distance in miles reported by the taximeter.</td>
    </tr>
    <tr>
        <td>Pickup_longitude</td>
        <td>Longitude where the meter was engaged.</td>
    </tr>
    <tr>
        <td>Pickup_latitude</td>
        <td>Latitude where the meter was engaged.</td>
    </tr>
    <tr>
        <td>RateCodeID</td>
        <td>The final rate code in effect at the end of the trip.
            <ol>
                <li> Standard rate </li>
                <li> JFK </li>
                <li> Newark </li>
                <li> Nassau or Westchester</li>
                <li> Negotiated fare </li>
                <li> Group ride</li>
            </ol>
        </td>
    </tr>
    <tr>
        <td>Store_and_fwd_flag</td>
        <td>This flag indicates whether the trip record was held in vehicle memory before sending to the vendor,<br> aka “store and forward,” because the vehicle did not have a connection to the server.
            <br>Y= store and forward trip
            <br>N= not a store and forward trip
        </td>
    </tr>
    <tr>
        <td>Dropoff_longitude</td>
        <td>Longitude where the meter was disengaged.</td>
    </tr>
    <tr>
        <td>Dropoff_latitude</td>
        <td>Latitude where the meter was disengaged.</td>
    </tr>
    <tr>
        <td>Payment_type</td>
        <td>A numeric code signifying how the passenger paid for the trip.
            <ol>
                <li> Credit card </li>
                <li> Cash </li>
                <li> No charge </li>
                <li> Dispute</li>
                <li> Unknown </li>
                <li> Voided trip</li>
            </ol>
        </td>
    </tr>
    <tr>
        <td>Fare_amount</td>
        <td>The time-and-distance fare calculated by the meter.</td>
    </tr>
    <tr>
        <td>Extra</td>
        <td>Miscellaneous extras and surcharges. Currently, this only includes. the $0.50 and $1 rush hour and overnight charges.</td>
    </tr>
    <tr>
        <td>MTA_tax</td>
        <td>0.50 MTA tax that is automatically triggered based on the metered rate in use.</td>
    </tr>
    <tr>
        <td>Improvement_surcharge</td>
        <td>0.30 improvement surcharge assessed trips at the flag drop. the improvement surcharge began being levied in 2015.</td>
    </tr>
    <tr>
        <td>Tip_amount</td>
        <td>Tip amount – This field is automatically populated for credit card tips.Cash tips are not included.</td>
    </tr>
    <tr>
        <td>Tolls_amount</td>
        <td>Total amount of all tolls paid in trip.</td>
    </tr>
    <tr>
        <td>Total_amount</td>
        <td>The total amount charged to passengers. Does not include cash tips.</td>
    </tr>
</table>

<br>

<p>
<strong>ML Problem Formulation :</strong>
</p>
<p><b><u> Time-series forecasting and Regression</u></b></p>
-<i> To find number of pickups, given location cordinates(latitude and longitude) and time, in the query reigion and surrounding regions.</i>
<p> 
To solve the above we would be using data collected in Jan - Mar 2015 to predict the pickups in Jan - Mar 2016.
</p>
