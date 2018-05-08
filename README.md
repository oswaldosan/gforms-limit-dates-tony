# gforms-limit-dates-tony


  Gravity Forms - date limiter 

    var d = new Date();   load the date 
    var dia = d.getDay()  load the specific day, Monday = 1, Tuesday = 2, wednesday = 3, thursday = 4 etc... 
    var hora = d.getHours();   load the hour 


    if (dia == '5' || hora > 9) {     Condition for check the specific day or hour

gform.addFilter( 'gform_datepicker_options_pre_init', function( optionsObj, formId, fieldId ) {
    if ( formId == 44 && fieldId == 1 ) {   Our form ID and field ID 
        optionsObj.minDate = +4;    DISABLE 4 DAYS FROM TODAY  
        optionsObj.onClose = function (dateText, inst) {
             jQuery('#input_44_1').datepicker('option', 'minDate', dateText).datepicker('setDate', dateText);
        };
    }
    return optionsObj;
});
 

} else {  


      /* DO stuff or not */

	 	 

}


Check the code.js to see the full code


