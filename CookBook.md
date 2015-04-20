a code book that describes the variables, the data, and any transformations or work that you performed to clean up the data called CodeBook.md.


**The main fuction** main(). Simple and clear. It runs the show, it knows where the dataset resides and it works with the other defined functions to get the job(s) done. I'm doing to take the comment right out of the code to describe the transforamtion.

<ol>
<li>Load and join the Y test and train together</li>
<li>Combine the Y train and test and row bind subjects together</li>
<li>Combine the x_train and x_test data and apply the headers ( Here we narrow the data set going after the columns that only contain mean and std) </li>
<li>Combine the all the data together</li>
<li>clean up the column heading names</li>
<li>record teh data to file</li>
<li>
</ol>

**tidy.txt MetaData**(#5 From the data set in step 4, creates a second, independent tidy data set with the average of each variable for each activity and each subject.) 

  **Column naming**
  <ol>
    <li>activity</li>
    <li>subject</li>
  </ol>
  
  The rest of the columns are obtained from cleaning up the column heading names which were:
  <ol>
  <li> obtained via a grep command only going after the columns with the following pattern(s) mean\\(\\)|std\\(\\)</li>
  <li> use gsub from 'mean' to 'Mean'</li>
  <li> use gsub from 'std' to 'Std'</li>
  <li> use gsub from '[()]' to '' remove it</li>
  <li> use gsub from '[-]' to '_' to simplify the tall tidy</li>
  <li> use gsub from 'BodyBody' to 'Body'
  </ol>


<ol>
<li>subject_id           </li>
<li>activity             </li>
<li>tBodyAcc_Mean_X      </li>
<li>tBodyAcc_Mean_Y      </li>
<li>tBodyAcc_Mean_Z      </li>
<li>tBodyAcc_Std_X       </li>
<li>tBodyAcc_Std_Y       </li>
<li>tBodyAcc_Std_Z       </li>
<li>tGravityAcc_Mean_X   </li>
<li>tGravityAcc_Mean_Y   </li>
<li>tGravityAcc_Mean_Z   </li>
<li>tGravityAcc_Std_X    </li>
<li>tGravityAcc_Std_Y    </li>
<li>tGravityAcc_Std_Z    </li>
<li>tBodyAccJerk_Mean_X  </li>
<li>tBodyAccJerk_Mean_Y  </li>
<li>tBodyAccJerk_Mean_Z  </li>
<li>tBodyAccJerk_Std_X   </li>
<li>tBodyAccJerk_Std_Y   </li>
<li>tBodyAccJerk_Std_Z   </li>
<li>tBodyGyro_Mean_X     </li>
<li>tBodyGyro_Mean_Y     </li>
<li>tBodyGyro_Mean_Z     </li>
<li>tBodyGyro_Std_X      </li>
<li>tBodyGyro_Std_Y      </li>
<li>tBodyGyro_Std_Z      </li>
<li>tBodyGyroJerk_Mean_X </li>
<li>tBodyGyroJerk_Mean_Y </li>
<li>tBodyGyroJerk_Mean_Z </li>
<li>tBodyGyroJerk_Std_X  </li>
<li>tBodyGyroJerk_Std_Y  </li>
<li>tBodyGyroJerk_Std_Z  </li>
<li>tBodyAccMag_Mean     </li>
<li>tBodyAccMag_Std      </li>
<li>tGravityAccMag_Mean  </li>
<li>tGravityAccMag_Std   </li>
<li>tBodyAccJerkMag_Mean </li>
<li>tBodyAccJerkMag_Std  </li>
<li>tBodyGyroMag_Mean    </li>
<li>tBodyGyroMag_Std     </li>
<li>tBodyGyroJerkMag_Mean</li>
<li>tBodyGyroJerkMag_Std </li>
<li>fBodyAcc_Mean_X      </li>
<li>fBodyAcc_Mean_Y      </li>
<li>fBodyAcc_Mean_Z      </li>
<li>fBodyAcc_Std_X       </li>
<li>fBodyAcc_Std_Y       </li>
<li>fBodyAcc_Std_Z       </li>
<li>fBodyAccJerk_Mean_X  </li>
<li>fBodyAccJerk_Mean_Y  </li>
<li>fBodyAccJerk_Mean_Z  </li>
<li>fBodyAccJerk_Std_X   </li>
<li>fBodyAccJerk_Std_Y   </li>
<li>fBodyAccJerk_Std_Z   </li>
<li>fBodyGyro_Mean_X     </li>
<li>fBodyGyro_Mean_Y     </li>
<li>fBodyGyro_Mean_Z     </li>
<li>fBodyGyro_Std_X      </li>
<li>fBodyGyro_Std_Y      </li>
<li>fBodyGyro_Std_Z      </li>
<li>fBodyAccMag_Mean     </li>
<li>fBodyAccMag_Std      </li>
<li>fBodyAccJerkMag_Mean </li>
<li>fBodyAccJerkMag_Std  </li>
<li>fBodyGyroMag_Mean    </li>
<li>fBodyGyroMag_Std     </li>
<li>fBodyGyroJerkMag_Mean</li>
<li>fBodyGyroJerkMag_Std  </li>
</ol>


at the end the end user will see the following messages to indicate the application has finished its work:

[1] "Done recordinng wide data tidywide"

[1] "Done recording narrow data tidyNarrow - Not part of requirements"

[1] "Done recording tidy  -- Final out put"

[1] "All done, enjoy the day."
