****Overview****
    The CalculateBusinessHrs class is an Invocable Apex class designed to calculate the duration (in hours) between two DateTime values,
    considering the Business Hours provided as input. This class is specifically useful for scenarios where you need to determine working hours between two points in time,
    excluding non-working hours, weekends, and holidays based on predefined Business Hours configurations in Salesforce.
    This class is particularly suitable for use in Salesforce Flows

****Class Structure****
    The CalculateBusinessHrs class contains the following components:

  1--calculateDuration Method:
    This is the main method marked as @InvocableMethod to be used in Salesforce Flows.
    Accepts a list of DurationInput objects and returns a list of DurationOutput objects.
  2--Inner Classes:
    DurationInput: Represents the input parameters for the method.
      StartTime: The starting DateTime value.
      EndTime: The ending DateTime value.
      BusinessHoursId: The ID of the Business Hours record to consider during calculation. Use get element in flow and filter by Name to get the desired business hours record,
    DurationOutput: Represents the output parameters from the method.
    DurationInHours: The duration between StartTime and EndTime in business hours.


****Use Cases****
    This class is ideal for calculating business hours in the following scenarios:

  --Support Case Management:
      Calculate the working hours between Case.CreatedDate and Case.ClosedDate to determine how long it took to resolve a case within business hours.
  
  --Service Level Agreement (SLA) Tracking:
      Determine the number of business hours it took to complete a task, opportunity stage change, or any custom business process.

  --Time Tracking for Approvals:
      Calculate how long an approval process took based on business hours defined for a specific team or department.

  --Employee Time Management:
      Measure time spent by employees on tasks or projects within business hours.
