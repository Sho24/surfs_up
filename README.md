# surfs_up

### Overview of the statistical analysis
 The overview of the project is to determine based on the available analysis data results for W. Avy to find more information about temperature trends before opening the surf shop specially in the months of June and December in Oahu,in order to determine if the surf and ice cream shop business is sustainable year-round.

    ## Results:

        ## The standerterd davisation of two different independent samples the temperature for June vs temperature for December across all available years in the dataset.

        Results: Dec_temp = 3.25, Dec_temp = 3.90           

        ## There is not sufficient evidence to conclude  there is a significant difference in means between June and December temperatures across all years available.

        Results: June_temp = 74.944118, Dec_temp = 71.041529

        ## There is a some difference in minimum between June and December temperatures across all years available.

        Results: June_temp = 64.00000, Dec_temp = 56.00000

    ## Summary:

        ## below are 2 session query use to get temperature results from sqllite database.

        June: June_results = session.query(Measurement.date, Measurement.tobs)\
                    .filter(extract("month", Measurement.date) == "6").all()
        
        December: december_results = session.query(Measurement.date, Measurement.tobs)\
                    .filter(extract("month", Measurement.date) == "12").all()
        
            