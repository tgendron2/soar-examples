# Artifact examples

***[Example]Prompt - create artifact*** is a simple playbook that prompts the user for three values (bass, treble, and volume). It creates an artifact calld "Hi fidelity" and saves the three values as key/values in the artifact. 
The example shows how to use  a format block to set up the values for the create artifiact utility. It needs an empty container to run off. 

***[Example]Artifact-update*** This example playbook adds a value to existing artifacts. It requires a container with artficat(s) named URL. Each artifact has a field called requestURL and you give it a url value to test with. 
The playbook filters by artifacts named URL and uses the requestURL as input to the whois app. the raw results returned by whois are added to the artifact in the field Raw.

In the events dashboard on Soar, use + Event to create a new event AKA a container. Then use the add artifact UI screren to add artficats named URL and add the requestURL value. 
