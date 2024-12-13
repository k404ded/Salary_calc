# Salary Calculator Prototype
# 2 leaves are paid leaves

# Input salary, holidays, and overtime
salary = int(input("Enter your salary: "))
holidays = int(input("Enter the number of holidays: "))
overtime = int(input("Enter the number of overtime hours: "))

# Constants
salary_per_day = salary / 30
overtime_rate = 150  # Overtime pay per hour
overtime_amount = overtime * overtime_rate

# Initialize amount deducted
amount_deducted = 0

# Calculate excess holidays
if holidays > 2:
    excess_holiday = holidays - 2
    amount_deducted = excess_holiday * salary_per_day
    print("Your excess holidays are:", excess_holiday)
    print("Amount deducted from your salary is:", amount_deducted)

# Calculate total salary
total_salary = salary - amount_deducted + overtime_amount

# Output results
print("Your salary per day is:", salary_per_day)
print("Your overtime amount is:", overtime_amount)
print("Your total salary for the month is:", total_salary)
