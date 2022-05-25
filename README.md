# managementsim
location of initial XSD docs for a Management Simulation Schema

Developed as part of a chapter called "Creating effective management simulations: rapidly, responsibly, relevantly!"

The XSD is a starting place to create a format simulations that can created by academics, businesses, and students and then consumed within a management simulation engine capable of reasing the XSD and returing a usable interface that enables the simulations to be tested, played, used in the classroom and evolved to reflect changing circumstances.

The proposed tags so far with their attributes and a rationale relating to their purpose 

- `<simulation>`
> The overall wrapper. All the aspects of the simulation would be defined within the tag and the resultant closing tag `</simulation>`
-  `<title>`
> The text contained by this and `</title>` offers human readable title of the simulation
-  `<sector>`
> The text contained by this and `</sector>` suggests the primary sector that the simulation would be most relevant for. This is primary human readily and does not impact on the functioning of the simulation
- `<scenario>`
> Another human readable text that provides a longer description of the simulation intended for helping people to chose a simulation rather than defining its functionality 
- `<author>` 
> A human readable version of the author's name contained between the `</author>` tag. 
> Potential attributes include `id="value"` where `value` may be an institutional id 
> `orcid="value" where `value` would be the author's ORCid provides opportunity for the author to link to a wider more recognisable system of researcher identification.
> More than one author could be defined in a single simulation
- `<revision>`
> Defines the current version of the simulation.  The text before `</revision>` may optionally offer some form of human readable description relating to version. The attribute `version="value"` would be expected to be a systematic machine readable version. Attribute `date="value"` would be an amibiguous date stamp either YYYY/MM/DD format or standard Unix timestamp.
- `<level>`
> Provides a human readable indicator of the intended audience for the simualtion. This may be a value such as `5` indicate UK study level or more generic phrasing such as `undergraduate`. The level does not affect functionality.
- `<documentation>`
> A description label held as text before `</documentation>` with an attribute `uri="value"` to indicate the location of more detailed documentation related to the simulation. The `value` is expected to be a URL or DOI and may point to an original source paper or other forms of output.
- `<participants />`
> One attribute `value="count"` where `count` would be a numeric value indicating the maximum number of players for the simulation. This value *may* be enforced by the simulation.
- `<time period="Daily|Weekly|Monthly|Quarterly|Annual" />`
- `<dimensions competitive="True|False" interactive="True|False" deteministic="True|False" tiered="True|False" />`
- `<teams value="True|False" allocation="random|determined" maxsize="" minsize="" />`
