[Работа с пациентами](../../../index.md)
=====================================

### ![POST](../../../../../img/post.png) [/patient/RcAppointment/add](../index.md)

```java
class AddPatientRcAppointment {
    public static void main(String[] args) throws IOException {
        final String code = "ТВК261129Ж";
        final ProtoBuffClient client = newProtoBuffClient();

        System.out.println();
        System.out.println("Поиск по коду " + code);
        top:
        for (Patients.Patient patient : client.searchPatients(Patients.PatientQuery
                .newBuilder()
                .setCode(code)
                .build())) {
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
                                    .setNote("Проверка")
                            )
                            .build());
                    break top;
                }
            }
        }

    }
}

```

**[HTTP примеры](add.md)**