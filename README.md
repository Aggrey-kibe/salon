# Salon Appointment Scheduler

A freeCodeCamp Relational Database certification project. A Bash script backed by a PostgreSQL database lets a customer choose a salon service and book an appointment.

## Files

- `salon.sh`: the interactive Bash script.
- `salon.sql`: a dump of the `salon` database.

## Database structure

- `customers`: `customer_id` (primary key), `phone` (unique), `name`
- `services`: `service_id` (primary key), `name`
- `appointments`: `appointment_id` (primary key), `customer_id` (foreign key), `service_id` (foreign key), `time`

## Usage

```bash
./salon.sh
```

The script:

1. Shows a numbered list of services, such as `1) cut`.
2. Shows the list again if the choice is not a valid service.
3. Asks for a phone number, and for a name if the customer is new.
4. Asks for a time and saves the appointment.
5. Prints a confirmation, for example `I have put you down for a cut at 10:30, Fabio.`

## Restoring the database

```bash
psql -U postgres < salon.sql
```

## Requirements

- PostgreSQL, with a `freecodecamp` user
- Bash
