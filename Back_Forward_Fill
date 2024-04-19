

Data want_2;
  do _n_ = 1 by 1 until (last.id);
    set have;
    by id;
    if missing(fisrt_k) and not missing(k) then
      first_k = k;
    end;

  prev_k = first_k

  do _n_ = 1 by 1 until (last.id);
    set have;
    by id;
    new_k = k;
    if missing(k) then
      new_k = prev_k;

    prev_k = new_k;
    output;
  end;
Run;


/******* Another way in the multiple SET example, to derive min, max and sum for the same dataset ****************************/
DATA newdata ;
  RETAIN minval maxval sumval ;
  IF ( _N_ eq 1 ) THEN DO UNTIL (lastrec) ;
    SET dsname_1 (keep = value) end = lastrec;
    minval = min ( minval, value ) ;
    maxval = max ( maxval, value ) ;
    sumval = sum ( sumval, value ) ;
  END ;

  SET dsname_1 ;
  ---------------------
RUN ;




