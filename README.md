# MyTripBudget
#Date: 05/09/2019
#Goal: Help travellers to organize and tracks their expenses on their short trips
#Technologies 
#Front end HTML 5 > CSS 3 > BOOTSTRAP > TypeScript ========= Framework: Angular 7
#Backend ASP.Net Core (C#) API
#RDBMS SQLServer

#Overview -> Track your expenses and stay on your budget
  1)- Admin setting dashboard
      User will enter how much he is willing to spend each day 
         Fields 1 => *Country *State *City *Trip Name *Starting Date *Return Date *Ticket
         Fields 2 => *Room *Xport *Food *Activities *Extra *Notes 
  2)- Button "Check Setting" => Displays each field with assigned values by the user + 'update' (if user wants to update data) 
  
  -----------------------
  System detect starting day (trip) 
    -System track the day after the trip starting day
           ->Check if user has entered his expenses of the previous day
                >if not sent alert ("What was your expenses yesterday ?") + btn to redirect to the form to get the expenses
           ->When user fills the form & submit
                   result_room = room_willing_to_spend - room_has_spent
                   result_food
                   result_xport
                   result_activities
                   result_extra
                >diplay
                   *room
                    willing to spend for the day ----- has spent -----color(if result_room >= 0 (green smiling face + mess)
                                                                                           > 0 (red shy face + mess))
                    *Chart (pie: initial color: orange) => based on # of days the trip will last, and what was spent for the particular field (in this case room)
                       if result_room >= 0 color of the day is green --------- result_room 'value' displays in green
                       if result_room < 0  color of the day is red   --------- result_room 'value' displays in red
                       
               > the day preceding the last day of the trip => App will display a report of the expenses for each field
                                  for specific field (e.g room)->  will make a comparison between amount_spent & total_amount_budgetized
                                                                   will make a comparison of total_spent and total_budgetized

 3)-In the future 
     ->Give option to the user to link images with his trip (bills, picture of a location, ....) 
	 ->Give option to the user tot login with one of his/her social network credential
	 