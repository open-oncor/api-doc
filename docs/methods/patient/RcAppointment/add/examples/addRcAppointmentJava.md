[Работа с пациентами](../../../index.md)
=====================================

### ![POST](../../../../../img/post.png) [/patient/RcAppointment/add](../index.md)

```java
class AddPatientRcAppointment {
    public static void main(String[] args) throws IOException {
        final ProtoBuffClient client = newProtoBuffClient();

        Patients.Patient patient = client.getPatient("70:33669");

        final List<Records.Rc> rcReferralList = client.getPatientRcReferralRLList(patient.getId());
        for (Records.Rc rc : rcReferralList) {
            final Records.Rc.RcReferral rcReferral = rc.getRcReferral();
            if (!rcReferral.hasRcAppointmentId()) {
                TestUtils.print(patient);
                final Records.Rc rcAppointment = client.addPatientRcAppointment(Records.Rc.newBuilder()
                        .setPatientId(patient.getId())
                        .setRcAppointment(Records.Rc.RcAppointment.newBuilder()
                                .setRcReferralId(rc.getId())
                                .setConfirmed(false)
                                .setNote("Example")
                        )
                        .build());
                TestUtils.print(rcAppointment);
            }
        }
    }
}

```

**[HTTP примеры](add.md)**