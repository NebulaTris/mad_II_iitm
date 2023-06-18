# JavaScript Graded Assignment - Simple and Compound Interest

Q) Write the definitions of the functions given below with the help of given information. </br>

```js
/*
 * calculateSimpleInterest calculates and returns the simple interest
 * (floor value) for a fixed deposit. Formula used is,

 * calculateSimpleInterest calculates and returns the simple interest
 * for a fixed deposit. Formula used is,
 * Simple Interest: P X R X T / 100
 *   where:
 *   P = Principal
 *   I = Daily interest rate
 *   N = Number of days
 *
 *  In case of any input error (wrong date format, alphabets in daily interest etc.), return -1
 *
 * @param {number} principal  - Principal amount
 * @param {number} dailyInterest  - daily interest rate
 * @param {string} startingDate  - Starting date of the fixed deposit in "YYYY-MM-DD" format, example "2015-03-25"
 * @param {string} endingDate  - Ending date of the fixed deposit in "YYYY-MM-DD" format, example "2015-03-25"
 * @return {number} interest
*/

/*
 * calculateCompoundInterest calculates and returns the compound interest
 * (floor value) for a fixed deposit. Formula used is,
 *   Compound Interest=P[(1+I/100)^N - 1]
 *   where:
 *   P = Principal
 *   I = Daily interest rate
 *   N = Number of days
 *
 *  In case of any input error (wrong date format, alphabets in daily interest etc.), return -1
 *
 * @param {number} principal  - Principal amount
 * @param {number} dailyInterest  - daily interest rate
 * @param {string} startingDate  - Starting date of the fixed deposit in "YYYY-MM-DD" format, example "2015-03-25"
 * @param {string} endingDate  - Ending date of the fixed deposit in "YYYY-MM-DD" format, example "2015-03-25"
 * @return {number} interest
*/

/*
 * extraAmountPercentage calculates and returns the extra amount percentage borrower will have to pay in case of
 * compound interest (floor value) in comparison to the simple interest for a fixed deposit.

 *  In case of any input error (wrong date format, alphabets in daily interest etc.), return -1
 *
 * @param {number} principal  - Principal amount
 * @param {number} dailyInterest  - Daily interest rate.
 * @param {string} startingDate  - Starting date of the fixed deposit in "YYYY-MM-DD" format, example "2015-03-25"
 * @param {string} endingDate  - Ending date of the fixed deposit in "YYYY-MM-DD" format, example "2015-03-25"
 * @return {number} percentage
*/

function calculateSimpleInterest(
  principal,
  dailyInterest,
  startingDate,
  endingDate
) {
    const startDate = new Date(startingDate);
  const endDate = new Date(endingDate);
  if (isNaN(startDate.getTime()) || isNaN(endDate.getTime()) || dailyInterest < 0) {
    return -1;
  }
  const timeDiff = Math.abs(endDate.getTime() - startDate.getTime());
  const diffDays = Math.ceil(timeDiff / (1000 * 3600 * 24));
  const interest = (principal * dailyInterest * diffDays) / 100;

return Math.floor(interest);

}

function calculateCompoundInterest(
  principal,
  dailyInterest,
  startingDate,
  endingDate
) {
    const startDate = new Date(startingDate);
    const endDate = new Date(endingDate);
    if (isNaN(startDate.getTime()) || isNaN(endDate.getTime()) || dailyInterest < 0) {
        return -1;
    }
    const timeDiff = Math.abs(endDate.getTime() - startDate.getTime());
    const diffDays = Math.ceil(timeDiff / (1000 * 3600 * 24));
    const interest = principal * (Math.pow((1 + dailyInterest / 100), diffDays) - 1);
    return Math.floor(interest);
}

function extraAmountPercentage(
  principal,
  dailyInterest,
  startingDate,
  endingDate
) {
    const simpleInterest = calculateSimpleInterest(principal, dailyInterest, startingDate, endingDate);
    const compoundInterest = calculateCompoundInterest(principal, dailyInterest, startingDate, endingDate);
    if (simpleInterest === -1 || compoundInterest === -1) {
        return -1;
  }
  const percentage = ((compoundInterest - simpleInterest) / simpleInterest) * 100;
return Math.floor(percentage);
}
```

