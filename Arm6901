// Copyright (c) FIRST and other WPILib contributors.
// Open Source Software; you can modify and/or share it under the terms of
// the WPILib BSD license file in the root directory of this project.

package frc.robot.subsystems;

import static edu.wpi.first.wpilibj.DoubleSolenoid.Value.kForward;
import static edu.wpi.first.wpilibj.DoubleSolenoid.Value.kOff;
import static edu.wpi.first.wpilibj.DoubleSolenoid.Value.kReverse;

import edu.wpi.first.wpilibj.DoubleSolenoid;
import edu.wpi.first.wpilibj.PneumaticsModuleType;
import edu.wpi.first.wpilibj2.command.CommandBase;
import edu.wpi.first.wpilibj2.command.SubsystemBase;
import frc.robot.Constants.GrabberConstants;

public class PneumaticGrabber extends SubsystemBase {

  private final DoubleSolenoid m_grabberSolenoid =
  new DoubleSolenoid(
      PneumaticsModuleType.CTREPCM,
      GrabberConstants.kGrabberSolenoidPorts[0],
      GrabberConstants.kGrabberSolenoidPorts[1]);

      private final DoubleSolenoid m_grabberSolenoid2 =
  new DoubleSolenoid(
      PneumaticsModuleType.CTREPCM,
      GrabberConstants.kGrabberSolenoidPorts[2],
      GrabberConstants.kGrabberSolenoidPorts[3]);

  /** Creates a new PneumaticGrabber. */
  public PneumaticGrabber() {
    m_grabberSolenoid.set(kOff);
    m_grabberSolenoid2.set(kOff);
  }

  // Open grabber
  public CommandBase openGrabber() {
    return runOnce(
        () -> {
          m_grabberSolenoid.set(kReverse);
          m_grabberSolenoid2.set(kReverse);
        });
  }

  // Close grabber
  public CommandBase closeGrabber() {
    return runOnce(
        () -> {
          m_grabberSolenoid.set(kForward);
        });
  }

  @Override
  public void periodic() {
    // This method will be called once per scheduler run
  }

  @Override
  public void simulationPeriodic() {
    // This method will be called once per scheduler run during simulation
  }
}
