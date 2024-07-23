@startuml
class MotorVehicle {
    +build(): void
}

class Motorcycle {
    +build(): void
}

class Car {
    +build(): void
}

abstract class MotorVehicleFactory {
    +create(): MotorVehicle
    -createMotorVehicle(): MotorVehicle
}

class MotorcycleFactory {
    -createMotorVehicle(): MotorVehicle
}

class CarFactory {
    -createMotorVehicle(): MotorVehicle
}

MotorVehicleFactory -> MotorVehicle : creates >
MotorcycleFactory -> Motorcycle : creates >
CarFactory -> Car : creates >

@enduml
