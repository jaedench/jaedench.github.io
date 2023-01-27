---
layout: essay
type: essay
title: "Smart Questions Save the Day"
# All dates must be YYYY-MM-DD format!
date: 2023-01-26
published: true
labels:
  - Questions
  - Answers
  - StackOverflow
---

<img width="350px" class="rounded float-start pe-4" src="../img/questions.png">

## Am I a Smart Question Asker?
As software engineers, we are expected to constantly think and solve problems. With this expectation, it comes as no surprise that we are expected to be good question-askers, however, this skill is not taught formally in classes. During my academic career, I often struggled with asking questions. I am naturally a shy person and hated speaking up in front of the class. Instead of asking the question I had, I often wondered whether or not it was a “stupid question.” 

Over the years, I have learned the importance of asking questions. After discussing with my classmates, I began to notice that I wasn’t the only one who had similar questions about certain topics. I would often wait to talk to my professors after class or during office hours about the things I was confused about. Although I felt more comfortable asking questions one on one, it didn’t mean I should ask whatever came to mind. 

How does one ask good questions? Being able to ask concise and intelligent questions is a crucial skill to develop not only in school but also in the workplace. Examples of good and bad or “smart” and “not smart” questions can be observed on a question and answer website for professional and enthusiast programmers called Stack Overflow.

## What Makes a Question Smart?
While asking a question, there are a few important steps that could save you time in receiving an answer and the person taking the time to help you. To ensure that you are asking a smart question, first, make sure you are asking an appropriate forum. To get a timely and quality response, it is helpful to have a meaningful and specific subject header that follows the format of “object - deviation,” where the object specifies what thing is having a problem, and the deviation describes how the outcome is different from the expected behavior. Reread your question to make sure you have expressed your thoughts clearly and grammatically correct. While looking over the question, be precise and informative about your problem. By taking the time to research on your own and include it in the question demonstrates that you understand the problem before asking the question. Make sure to state exactly what is wrong and not what you think it could be. All of these techniques methods and techniques will help software engineers ensure that the questions they ask are “smart.”

## Not Smart, Stupid, Silly Questions
To start, let’s look at an example of a “not smart” question. A Stack Overflow user asked, ["Javascript: Simple addition program not working"](https://stackoverflow.com/questions/32562260/javascript-simple-addition-program-not-working). 

```

Q: Javascript: Simple addition program not working

I'm trying to create a program that'll add two numbers when clicked on a button.

However, it's not working, I am totally confused what's wrong. In this program user is supposed to enter 2 numbers and program gives user the sum on the click

Here's the Code:

<html>

    <body>
        <p>For adding two numbers</p>

        <button onclick="myFunction()">Calculate</button>
        <br/>
        <input type="text" placeholder="1st number" id="1st" name="txt1">
        <br/>+
        <br/>
        <input type="text" placeholder="2nd number" id="2nd" name="txt2">

        <p id="demo"></p>

        <script>
        function myFunction() {
            var a = document.getElementById("1st").value;
            var b = document.getElementById("2nd").value;
            var c = number(a) + number(b);

            document.getElementById("demo").innerHTML = c;
        }
        </script>
    </body>

</html>

```

This is a not smart question because it does not have a meaningful and specific subject header. Instead of just saying that the program wasn’t working, they could’ve stated the error message or how the output was differing from what was expected. The user could have also included more information in the summary, such as the error message or what the program was being run on to give a viewer a little more insight. After reading the header, I still wasn’t sure if the problem was that the sum was incorrect, the button didn’t work, or the program didn’t compile at all. Based on the responses, the question was not very smart because it was just a simple fix of capitalizing a function. This question taught me the importance of taking the time to research and understand the syntax of a language before asking a not smart question.

## Smart, Successful, Stunning Questions
Now, let’s look at an example of a “smart” question. A Stack Overflow user asked, [“java.lang.NumberFormatException: Invalid int: ‘24 pm’”](https://stackoverflow.com/questions/43362754/java-lang-numberformatexception-invalid-int-24-pm). 

```

Q: java.lang.NumberFormatException: Invalid int: "24 pm"

My app crashed when I choose time using a TimePicker.
How to fix this?

Please guide me.

when I print the timeMinute System.out: 30 am I get an error on this line Integer.parseInt(timeMinute.replace(" am","")), true);

start_time.setInputType(InputType.TYPE_NULL);

        start_time.setOnClickListener(new View.OnClickListener() {

            @Override
            public void onClick(View v) {
                String time = start_time.getText().toString();

                if (time != null && !time.equals("")) {
                    StringTokenizer st = new StringTokenizer(time, ":");
                    String timeHour = st.nextToken();
                    String timeMinute = st.nextToken();

                    timePickDialog = new TimePickerDialog(v.getContext(),
                            new TimePickHandler(), Integer.parseInt(timeHour),
                            Integer.parseInt(timeMinute.replace(" am","")), true);

                } else {
                    timePickDialog = new TimePickerDialog(v.getContext(),
                            new TimePickHandler(), 10, 45, true);
                }
                timePickDialog.show();
            }
        });

private class TimePickHandler implements TimePickerDialog.OnTimeSetListener {

        @Override
        public void onTimeSet(TimePicker view, int hourOfDay, int minute) {
            //start_time.setText(hourOfDay + ":" + minute);
            int hour = hourOfDay % 12;
            if (hour == 0)
                hour = 12;
            start_time.setText(String.format("%02d:%02d %s", hour, minute,hourOfDay < 12 ? "am" : "pm"));
            timePickDialog.hide();
        }
    }

```

This is an example of a smart question because the subject header provides the type of language the person is using and the error that they are running into. The user has tried to print out certain aspects of the program, which shows they are attempting to understand what the problem is before asking a question. Also, the user provides which line is associated with the error message to help others quickly understand where to look in the appropriately included code. The responses reflect that this question was smart because no one asked for more clarification and similar to the question itself, the answers were also stated precisely. From this question, I was able to better understand that asking concise and informative questions can lead to effective answers that are easy to understand as well.
