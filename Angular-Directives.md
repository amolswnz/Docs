#Pagination
    <dir-pagination-controls></dir-pagination-controls>
    <tr dir-paginate="customer in customers 
                        | orderBy: '-totalBookings' 
                        | itemsPerPage: pageSize track by $index"
                         current-page="currentPage">                            
        <td> {{ ($index + 1) + (currentPage - 1) * pageSize }} </td>
        <!-- For maintaining the current item number in list  -->
   
    <script src="js/directives/dirPagination.js"></script>


#Loading bar 
    <!-- Advantage no need to add any code anywhere in any file -->
    <link rel='stylesheet' type="text/css" href='css/loading-bar.css'/>
    <script src='js/lib/loading-bar.min.js'></script>


#Notification messages
    <link rel="stylesheet" type="text/css" href="css/toastr.min.css">
    <script src="js/lib/toastr.min.js"></script>

    toastr.warning("No data updated !");

    toastr.success("Booking details updated.");
    setTimeout(function() { window.location.href = "/ng-admin"; }, 2000);


#Filters 
    /* Generate series of number from to */
    app.filter('range', function() {
        return function(input, total) {
            total = parseInt(total);
            for (var i = 0; i < total; i++) {
                input.push(i);
            }
            return input;
        };
    });

    /* Custom filter to change the MySQL date string to JavaScript Date String -> required for sorting */ 
    app.filter('dateToISO', function() {
        return function(input) {
            // Bug fix for undefined input 
            if(input === undefined) {
                return true;
            }
            else {
                return new Date(input).toISOString();
            }
        };
    });

    /*  To remove the following error
        Error: [filter:notarray] This might be related to a breaking change in angular 1.5 
        Answered here -> http://stackoverflow.com/questions/36448826/error-orderby-when-updating-to-angular-1-5-3
    */ 
    app.filter('toArray', function() {
        return function(obj, addKey) {
            if (!angular.isObject(obj)) return obj;
            if (addKey === false) {
                return Object.keys(obj).map(function(key) {
                    return obj[key];
                });
            } else {
                return Object.keys(obj).map(function(key) {
                    var value = obj[key];
                    return angular.isObject(value) ?
                        Object.defineProperty(value, '$key', {
                            enumerable: false,
                            value: key
                        }) : {
                            $key: key,
                            $value: value
                        };
                });
            }
        };
    });