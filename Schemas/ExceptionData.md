
#AI.ExceptionData
Instance of Exception represents handled or unhandled exception that occurred during execution of the monitored application.
## ver: int
Schema version

Default value: 2

## handledAt: string
Indication of where exception was caught to assess it's severity. Possible values are 'user code' (UserCode), 'framework' (Platform) or 'unhandled' (Unhandled)

**Question**: Should we deprecate it?

Max length: 9

## exceptions: IList[ExceptionDetails]
Exception chain - list of inner exceptions.

[ExceptionDetails] "Exception details of the exception in a chain."
    - id: int
    In case exception is nested (outer exception contains inner one), the id and outerId properties are used to represent the nesting.
    
    This field is optional.
    
    - outerId: int
    The value of outerId is a reference to an element in ExceptionDetails that represents the outer exception
    
    This field is optional.
    
    - typeName: string
    Exception type name.
    
    Max length: 1024
    
    - message: string
    Exception message.
    
    Max length: 1024
    
    - hasFullStack: bool
    Indicates if full exception stack is provided in the exception. Stack may be trimmed, such as in the case of StackOverflow exception.
    
    Default value: true
    
    This field is optional.
    
    - stack: string
    Text describing the stack. Either stack or parsedStack should have a value.
    
    Max length: 32768
    
    This field is optional.
    
    - parsedStack: IList[StackFrame]
    List of stack frames. Either stack or parsedStack should have a value.
    
    This field is optional.
    
    [StackFrame] "Stack frame information."
        - level: int
        Level in the call stack. For the long stacks SDK may not report every function in a call stack.
        
        - method: string
        Method name.
        
        Max length: 1024
        
        - assembly: string
        Name of the assembly (dll, jar, etc.) containing this function.
        
        Max length: 1024
        
        This field is optional.
        
        - fileName: string
        File name or Url of the method implementation.
        
        Max length: 1024
        
        This field is optional.
        
        - line: int
        Line number of the code implementation.
        
        This field is optional.
        
        
    
## severityLevel: test.SeverityLevel
Severity level. Mostly used to indicate exception severity level when it is reported by logging library.

This field is optional.

[SeverityLevel] "Defines the level of severity for the event."
    - Verbose = 0
    - Information = 1
    - Warning = 2
    - Error = 3
    - Critical = 4
    
## problemId: string
Identifier of where the exception was thrown in code. Used for exceptions grouping. Typically a combination of exception type and a function from the call stack.

**Question**: This is a new limit. It is aligned with other names. Verify it's ok

Max length: 1024

This field is optional.

## crashThreadId: int
The crashing thread id for Windows Store apps.

**Question**: Is it used by any of SDKs? Should it be deprecated?

This field is optional.

## properties: IDictionary[string, string]
Collection of custom properties.

Max key length: 150

Max value length: 8192

This field is optional.

## measurements: IDictionary[string, double]
Collection of custom measurements.

Max key length: 150

This field is optional.

