# assignment-5
Q1:
# To find the ultimate moment carring capacity of singly r/f beam
 fck = float(input("Enter the value of charateristics compressive strength:"))
 fy= float(input("Enter the grade of steel:")
 Es = float(input("Enter the value of Modulus of Elasticity of steel:"))
b= float(input("Enter the value of Width: ")
d= float(input("Enter the value of effective depth:"))
 d1 = float(input("Enter the value of bar diameter (d1):")
d2 = float(input("Enter the value of bar diameter (d2):")
n=int(input("Enter the number of bars")
Ast1= (n*0.7854*d 1*d1)
 Ast2= (n*0.7854*d2*d2)
 print ("The value of area of steel (Ast1):", Ast1)
 print ("The vaiue of area of steel (Ast2):", Ast2)
 # Total area of steel
 Ast = Astl + Ast2
print ("The value of area of steel (Ast):", Ast)
 # Neutral Axis Factor
 ku = 0.0035/(0.0055 + (fy/(1.15*Es))
 print ("The value of Neutral axis factor (ku):", ku)
# Momenent of Resistance factor
 Ru= 0.36*fck*ku*(1-(0.42*ku)
 print ("The value of Moment of Resistance factor (Ru):", Ru)
 # Maximum Neutral Axis:
 xumax = ku*d
print ("The value of maximum neutral axis (xumax):", xumax)
 xu = (0.87 *fy*Ast)/(0.36*fck*b)
 print ("The value of Actual Neutral Axis (xu):", xu)
 if xumax>xu:
 print ("UNDER REINFORCED")
 else:
 print ("OVER REINFORCED")
 # By Comparing
 X = float(input("Enter the value of Neutral Axis:")
 # Moment of Resistance
 print ("The value of Moment of Resistance is:", Mu)


 Q2
 # Design of Slab
 # Given Data
 # Effective span is already given in question
 span= span float(input("Enter the value of effective span in meters:"))
 b= float(input("Enter the value of width of slab in mm:")
 bs= float(input("Entert the value of Support Width in meters:")
 fck float(input(" Enter the value of Characteristics Compressive Strength:"))
 fy = float(input('"Enter the value of grade of steel:")
 Es float (input("Enter the value of Modulus of Elasticity is:")
 LL = float(in put("Enter the value of Live Load:"))
 FF = float(input("Enter the value of Floor Finish:")
 Density float(input("Enter the value of Density of RCC:"))
 # Design Constants
 # Neutral Axis Factor
 ku 0.0035/((0.0055)+ (fy/(1.15 Es))
 print ("The value of Neutral Axis Factor (ku) is:", ku)
 # Moment of Resistan ce Facor
Ru= 0.36*fck*ku (1-(0.42*ku))
 print ("The value of Moment Resisteance factor (Ru) is:", Ru)
 # Assurming pt 0.5 from fig.4 from IS 456:2007 page no.38
 fs float(input("Ent er the value of Steel Stress of Service:")
 # From Graph find out the Modification Factor
 MF float(input("Enter the value of Modification Factor:"))
 #From Clause 23.2.1 Select span/d Ratio
 S= float(input("Enter the value of span/d ratio:")
 # Correction Factors
 k1 float(input("Enter the value of Correction factor if sapn> 10m (k1):")
 k2= float(input(" Enter the value of Tension r/f correction factor (k2):")
 k3= float(input ('enter the value of Compression r/f correction factor (k3):")
 k4= float (input(" Enter the value of correction factor in case of flanged section (k4):")
 # Effective depth
 d1= (span*1000)/(S*MF*k1"k2k3*k4)
 print ("The value of effective depth as per deflection criteria is:", di)
 # Define Effective depth and overall depth Assuming value of cover
 d = float(input("Enter the value of Effective depth in mm (d):")
 D= float(input("Enter the value of Overall depth in mm (D):")
 # Load Calculations
 # Self Weight of slab
 DL = D*Density/1000
print ("The Dead load is:", DL)
 # Total Load is
 Factor float(input("Enter the value of partial Safety Factor is: ")
 TL = DL + LL + FF
 print ("The value of total load is:", TL)
 Wu Factor*TL
 print ("Wu=", Wu)
 # Bendingf Moment Calculations (Mu)
 Mu= Wu*span*span/8
 print ("The Value of Bending Moment (Mu) is:", Mu)
 # Check for effective depth
 d2 (Mu 100000O/(Ru*b))**0.5
 print ("The value of Effective depth as per Mornent criteria:", d2)
 if d2>d:
 print ("Revise the Depth:")
 else:
 print ("'SAFE")
 d = float(input ('"Enter the value of Effective depth in mm (d):")
 print ("Minimum Steel Calculations")
 Astmin = 0.12*b*D/100
 print ("The value of Minimum steel is:", Astmin)
print ("Main Steel calculations'")
 Ast (0.5 fck*b*d)/(fy))(1-(1-(4.6*Mu*1000000)/(fck *b*d*d))) "0.5))
 print ("Ast:", Ast)
 print ("Check for Ast")
 if Ast<Astmin:
 print ("Take Ast=Astmin")
 else:
 print ("Ast>Astmin, Hence SAFE")
 dial = float(in put("Enter the value of bar diameter for main steel:")
 dia2 = float(input(" Enter the value of bar diameter for Distribution steel:"))
# Area of bar
 aol = 0.7854*dia1*dial
 print ("The Value of Area of main steel bar (ao1):", ao1)
 a02= 0.7854* dia2*dia2
 print ("The Value of Area of main steel bar (ao2):", a02)
 # Sapcing Calculations
 Spacing1 = ao1*b/Ast
 print ("The sapcing for main steel bars is;", Spacing1)
 Spacing2 = ao2*b/Astmin
 print ("The sapcing for distribution steel bars is;", Spacing2)
 print ("Check 1 for main steel")
 if Spacing1>300:
 print ("UNSAFE")
 else:
 print ("SAFE")
 print ("'Check 2 for main steel")
 if Spacing1> "d:
 print ("UNSAFE")
elsc:
 print ("SAFE")
 print ("Check 1 fon Distribution steel")
 if Spacing1>300:
 print ("UNSAFE")
 else:
 print ("SAFE")
 print ("Check 2 for Distribution steel")
 if Spacing 1>5*d:
 print ("UNSAFE")
 else:
 print ("'SAFE")
 print ("'Approximated values of Sapcing:")
 S1 float(in put("Enter the value of spacing of main bars:")
 S2 float(in put("Enter the value of spacing of distribution bars:")
 Astprovided ao1*b/S1
 print ("The provided steel area for main bars at section in mm^2 is:", Astprovided)
 Astprodist ao2 b/52
 print ("The provided steel area for distribution bars at section in mm^2 is: ", Astprodist)
 # Check for Shear
 Vu = (Wuspan/2)-(Wu*((bs/2)-(d/1000)))
 print ("The value of SF at a Section is:", Vu)
 SStress = (Vu*1000)/(b*d)
 print ("The vaiue of shear stress is:", SStress)
 # From table 20 IS 456:2007 page 73
 SStressmax = float(input("Enter the value of maximum Shear stress:")
 if SStress>SStressmax:
 print ("Crushing will happen")
 else:
 print ("SAFE")
 # Percentage Steel
 pt =(100 Ast)/ (b *d) 120
 print ("Enter the value of percentage steel is:", pt)
 # From table 19 IS 456:2007 page 73
 SS= float (input("Enter the value of Shear Stress is:"))
 k= float(input("Enter the value of depth factor:")
 Shear k*SS
 print ("The value of shear at section is, Shear)
 if SStress>Shear:
 print ("Shear Reinforcement Required")
 else:
 print ("Shear Reinforcement not Required, SAFE")
 # Check for Deflection
 ActDEF = span*1000/d
 print ("The value od span/d is:", ActDEF)
 # Actual Deflection
 MaxDEF = S*ME*k1*k2*k3*k4
 print ("The permissible deflection is:", MaxDEF)
 if MaxDEF>S/d:
 print ("SAFE")
 else:
 print ("UNSAFE")
 # Check for Anchorage Length
 M1 = 0.87*fy*Ast* (d (fy*Ast)/(fck*b)) -
 print ("The value of Moment (M1)'", M1)
 lo = 8*dial
 La = 1.3*(M1/Vu)+10
 print ("The value of Anchorage length is:", La)
 # Development Length
 bonds = float(input("Enter the value of Bond Stress:")
 Ld = 0.87 *fy*dia1/4* bondS *1.6
 print ("The value of Development length is:", Ld)
 if La>Ld:
 print ("'SAFE")
 else:
 print ("increase anchorage")
