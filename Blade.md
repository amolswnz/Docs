#Blade Templating Engine

##Layout files
 * @yield('sectionName')  // In fileName.blade.php
    
 * /* In your views files */
    @extends('folderName.fileName')
    @section('sectionName')
        // ...
    @stop

##Partials include
 * @include('folderName.fileName')

##Control Structures
 * @if(express)
   @else
   @endif

 * @for(expression)
   @endfor

##Cross Site Scripting Protection
 * By default it is on
 {{ "<strong>Some text</strong>"  }} will output
 <strong>Some text</strong>
 * To print HTML code inside {{ }}
 {!! "<strong>Some text</strong>" !!} will output
 **Some Text**
 
