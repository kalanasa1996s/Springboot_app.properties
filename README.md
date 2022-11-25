# Springboot_app.properties
Spring Boot application.properties File Configuration


    spring.jpa.hibernate.ddl-auto=update
    spring.datasource.url=jdbc:mysql://localhost:3306/yourdbName?useSSL=false&createDatabaseIfNotExist=true&serverTimezone=Asia/Colombo
    server.port=8081
    spring.datasource.username=root
    spring.datasource.password=password
    spring.datasource.driver-class-name=com.mysql.cj.jdbc.Driver
    spring.jpa.show-sql=true



VarList Class ---
    
        public class VarList {

        public static final String RSP_SUCCESS              = "00";
        public static final String RSP_NO_DATA_FOUND        = "01";
        public static final String RSP_NOT_AUTHORISED       = "02";
        public static final String RSP_TOKEN_EXPIRED        = "03";
        public static final String RSP_TOKEN_INVALID        = "04";
        public static final String RSP_ERROR                = "05";
        public static final String RSP_DUPLICATED           = "06";
        public static final String RSP_FAIL                 = "10";
    }
    
    

ResponseDTO ---

        @Component
        @AllArgsConstructor
        @NoArgsConstructor
        @Data
        public class ResponseDTO {
            private String code;
            private String message;
            private Object content;
        }
