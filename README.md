def calculate_lift(rho, velocity, wing_area, lift_coefficient):
    """
    Calculate lift force using the lift equation:
    L = 0.5 * rho * V^2 * S * CL
    """
    return 0.5 * rho * velocity ** 2 * wing_area * lift_coefficient
 
print("Constant Input")
try:
    lift_coefficient = float(input("Enter the Lift Coefficient (C_L): "))
    rho_initial = float(input("Enter the Air Density (kg/m^3): "))
except ValueError:
    print("Invalid input. Please enter numeric values.")
    exit()
 
print("\nVariable Input")
try:
    velocity = float(input("Enter the Velocity (m/s): "))
    rho = float(input("Enter the Air Density again (kg/m^3): "))
    wing_area = float(input("Enter the Wing Area (m^2): "))
except ValueError:
    print("Invalid input. Please enter numeric values.")
    exit()


lift_force = calculate_lift(rho, velocity, wing_area, lift_coefficient)
print(f"\n✈️ Calculated Lift Force: {lift_force:.2f} Newtons")
