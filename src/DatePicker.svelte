<script>
import jQuery from 'jquery'
import moment from 'moment'
import daterangepicker from 'daterangepicker'
   

    export let dateContainerID = "#dateRange"


    //child to parent - Sab
    export let onChange
    let DateSelected = ''
    $: onChange(DateSelected)

  
    jQuery(function()
    {
      jQuery((dateContainerID)).daterangepicker
        (
          {
            ranges: 
            {
                'opens': 'center',
                'Today': [moment(), moment()],
                'Yesterday': [moment().subtract(1, 'days'), moment().subtract(1, 'days')],
                'Last 7 Days': [moment().subtract(6, 'days'), moment()],
                'Last 30 Days': [moment().subtract(29, 'days'), moment()],
                'This Month': [moment().startOf('month'), moment().endOf('month')],
                'Last Month': [moment().subtract(1, 'month').startOf('month'), moment().subtract(1, 'month').endOf('month')]
            },
            
            "alwaysShowCalendars": true,
            "startDate": moment(),
            "endDate": moment(),
            "opens": "right",
          }, function(start, end) 
            {
                //child to parent - Sab
                DateSelected = start.format('YYYY-MM-DD') + ' to ' + end.format('YYYY-MM-DD')
                
                console.log('New date range selected: ' + start.format('YYYY-MM-DD') + ' to ' + end.format('YYYY-MM-DD'))
            
            }
        )
    })

    
  </script>