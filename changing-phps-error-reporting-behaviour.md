### Changing PHP’s Error Reporting Behaviour

Error Reporting can be changed by using PHP settings and\/or PHP function calls. Using the built in PHP function error\_reporting\(\) you can set the level of errors for the duration of the script execution by passing one of the predefined error level constants, meaning if you only want to see Warnings and Errors - but not Notices - then you can configure that:

error\_reporting\(E\_ERROR \| E\_WARNING\);

You can also control whether or not errors are displayed to the screen \(good for development\) or hidden, and logged \(good for production\). For more information on this check out the [Error Reporting](http://phpdevenezuela.github.io/#error_reporting) section.

