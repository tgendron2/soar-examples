# Artifact examples

***[Example]Prompt - create artifact*** is a simple playbook that prompts the user for three values (bass, treble, and volume). It creates an artifact calld "Hi fidelity" and saves the three values as key/values in the artifact. 
The example shows how to use  a format block to set up the values for the create artifiact utility. It needs an empty container to run off. 

***[Example]Artifact-update*** This example playbook adds a value to existing artifacts. It requires a container with artficat(s) named URL. Each artifact has a field called requestURL and you give it a url value to test with. 
The playbook filters by artifacts named URL and uses the requestURL as input to the whois app. the raw results returned by whois are added to the artifact in the field Raw.

In the events dashboard on Soar, use + Event to create a new event AKA a container. Then use the add artifact UI screren to add artficats named URL and add the requestURL value. 

***[Example]data_parse4_cf*** An example showing how to get a individual lists. I could not reference the individual items in the list with the datapath picker. Insteadn I show a couple techniques using two format blocks and alternatively a code block. These would be used to end individual items down stream.  It is depended on a custom function datapath_format_test (1) mainly becuase I thought that would help define a proper datapath. 

Note that this example is one way of doing it. Datapath reference could still be a possibility but it is not obvious how to get it done, not have I found an example in the documentation. 

***datapath_format_test (1)*** The custom function that is used in the data parse4_cf example. You will have to modify the utlilty blick that calls the function so that it references you repo
See phantom.custom_function(custom_function="ods_dev_work/datapath_format_test", parameters=parameters, name="datapath_format_test_4", callback=show_cf_list) The string "ods_dev_work will have to be changed to link to the repo you save        this in on your enviornment. That it could be "local" but may not depending on how your source control is configured. 


