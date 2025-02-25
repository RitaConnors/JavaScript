"use strict";

const $ = selector => document.querySelector(selector);

const getErrorMsg = lbl => `${lbl} must be a valid number greater than zero.`;

const focusAndSelect = selector => {
    const elem = $(selector);
    elem.focus();
    elem.select();
};

const processEntries = () => {
    const miles = parseFloat($("#miles").value);
    const gallons = parseFloat($("#gallons").value);

    if (isNaN(miles) || miles <= 0) {
        alert(getErrorMsg("Miles driven"));
        focusAndSelect("#miles");
    } else if (isNaN(gallons) || gallons <= 0) {
        alert(getErrorMsg("Gallons of gas used"));
        focusAndSelect("#gallons");
    } else {
        $("#mpg").value = (miles / gallons).toFixed(2);
    }
};

var clearEntries = () => {
    $("#miles").value = "";
    $("#gallons").value = "";
    $("#mpg").value = "";
};

var clearMiles = () => {
    $("#miles").value = "";
}

var clearGallons = () => {
    $("#gallons").value = "";
}

document.addEventListener("DOMContentLoaded", () => {
    $("#calculate").addEventListener("click", processEntries);
    $("#mpg").addEventListener("dblclick", clearEntries);
    $("#miles").addEventListener("focus", clearMiles);
    $("#gallons").addEventListener("focus", clearGallons);
    $("#gallons").addEventListener("blur", processEntries);
    $("#miles").focus();
});
