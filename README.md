# Vacation-Tracking-System
This repo consists of system analaysis diagrams for a Vacation Tracking System

## Pseudocode

```code
Function createLeaveRequest() {
    var vacationType = getVacationType();
    var vacationHours = getHours()
    var vacationStartDate = getStartDate();
    var vacationEndDate = getEndDate();
    var EmployeeID = getEmployeeID();
    
    return new LeaveRequest(vacationType, vacationHours, vacationStartDate, vacationEndDate, EmployeeID)
}

Function manageTime(LeaveRequest request) {
    if(isNotValid(request)) {
        error = IN_VALID_REASON;
        return CREATE_REQUEST_FORM;
    }
    
    if(isManagerApprovalRequired(request)) {
        sendEmailToManager(request);
    }
    
    return HOME_PAGE;
}

Function managerController() {
    List pendingRequestsList = getPendingRequests();
    foreach (request : pendingRequestsList) {
        makeRequestDecision(request);
        updateRequestStatus(request);
        notifyRequestOwner(request);
    }
    return HOME_PAGE;
}
```
