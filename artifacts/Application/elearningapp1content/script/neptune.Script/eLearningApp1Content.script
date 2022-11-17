function submit(){

    // Clear all current ValueStates
    inputName.setValueState("None");
    inputPN.setValueState("None");
    inputLat.setValueState("None");
    inputLong.setValueState("None");
    datePickerCheckup.setValueState("None");

    // **** VALIDATION SECTION ******
    //Use "Return" to get out of the script
    if (inputName.getValue() === ""){
        inputName.setValueState("Error")
        sap.m.MessageToast.show("Please provide a Name");
        return
    };

    if (inputPN.getValue() === ""){
        inputPN.setValueState("Error")
        sap.m.MessageToast.show("Please provide a Part Number");
        return
    };

    if (inputLat.getValue() === ""){
        inputLat.setValueState("Error")
        sap.m.MessageToast.show("Please provide a Latitude");
        return
    };

    if (inputLong.getValue() === ""){
        inputLong.setValueState("Error")
        sap.m.MessageToast.show("Please provide a Longitude");
        return
    };

    if (datePickerCheckup.getValue() === ""){
        datePickerCheckup.setValueState("Error")
        sap.m.MessageToast.show("Please provide a Installation Date");
        return
    };

    if (sliderInterval.getValue() === 0){
        sap.m.MessageToast.show("Please provide a Service Interval");
        return
    };

    // Create the empty Object
    let final_data = {}

    // Add attributes to the Object, based on the inputs
    final_data.name = inputName.getValue();
    final_data.part_number = inputPN.getValue();
    final_data.latitude = inputLat.getValue();
    final_data.longitude = inputLong.getValue();

    // NOTE: getDateValue() used for the datePicker, instead of .getValue()
    final_data.checkup_date = datePickerCheckup.getDateValue();

    final_data.checkup_interval = sliderInterval.getValue();

    // PDF is optional
    // The "?" here, means if no PDF data exists, it will be set to an empty string
    final_data.pdf = pdfEncoding.getText() ? pdfEncoding.getText() : "" ;

    // Log the Object
    console.log(final_data);

    // Assign the data object to "Options"
    var options = {data: final_data};
    // Trigger the API and pass the "Options"

    apiaddEquipment(options);
    // Call the clearForm function
    clearForm();

}


function clearForm(){

    let getValcomponents = [inputName, inputPN, inputLat, inputLong, datePickerCheckup];
    // Arrow function:
    getValcomponents.forEach(component => component.setValue(""));
    // ForEach of the components listed above, set the values to an empty string
    
    // Handle these seperately
    oPDFViewer.setSource("");
    oPDFViewer.setVisible(false);
    pdfEncoding.setText("");
    pdfUpload.setValue("");
    pdfUpload.setVisible(false);
    checkboxSelected.setSelected(false);
    
    //Sliders have integers as values and therefore can be set to zero.
    sliderInterval.setValue(0);
    //Reset the label
    labelDays.setText("Service interval");
}
