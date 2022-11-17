// Map variable requires declaring!
var Map;

// IF in launchpad, get the ID
if (sap.n) {
    var localViewID = this.getId();
}

function populateInspectionJobPage(data) {

    // Set 'data' to the Page Model

    // Always start on the (first) Comments panel

    // ----- MAP -----
    // Check if Map component exists

    // If NOT already rendered on the page...
    if (jobLocationMapDiv === null) {
        // --- Build Map ---
        console.log("Build Map")

        // Navigate to the page
        // (Need to load the page before we can set the map)

        // Check if running on a Launchpad...
        // Handle the localViewID prefix if so


        // setView(Lat, Long , Zoom level)

    } else {
        // --- Update Map ---
        console.log("Update Map")

        // Navigate to the page
        oApp.to(viewInspectionJob);
    }

    // ----- Inspection Data -----
    // Check if any inspection data is already present, if so, 
    // populate and the mark section complete

    // Flag - Will be set to false if any data 
    // (from the Comments, Attachments, Barcode & Signature)
    // isn't present..
    var isAllDataPresent = true;

    // For each section
    // If the data is missing, reset the page...
    // If the data is present, set it to the correct component!
    // 1/4 - Comments


    // 2/4 - Picture


    // 3/4 - Barcode


    // 4/4 - Signature


    // After loading in the data, if all data is present
    // Set an invisible text element in the page footer to 'true'

    // This is so when navigating away from a complete inspection draft
    // No navigation confirmation box will be shown


    //checkIfReadyToSubmit();

}

function checkIfReadyToSubmit() {

    // Check state of each tab

    // If all colors are not "Default", enable Submit button

}

function collateInspectionData() {

    var inspectionObject = {}

    // Check if saved data present for each section
    // If so, add it
    // Otherwise, add "null"

    return inspectionObject;

}

function savePartialInspectionAndNavigate() {

    sap.m.MessageToast.show("Saving draft...");

    var draftData = collateInspectionData();
    console.log("draftData:");
    console.log(draftData);

    // Update inspection record with data
    // with a Where = part_number
    
    // Navigate to main page and re-trigger getInspectionList


}

function submitInspection() {

    sap.m.MessageToast.show("Submitting Inspection...");

    var inspectionData = collateInspectionData();
        inspectionData.status = "Submitted";
    console.log("inspectionData:");
    console.log(inspectionData);

    // Update inspection record with data
    // with a Where = part_number

    // Navigate to main page and re-trigger getInspectionList

}