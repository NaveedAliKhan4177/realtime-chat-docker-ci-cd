# ---------- Build stage ----------
FROM node:20-alpine AS builder
WORKDIR /app
COPY package*.json ./
RUN npm install --production
COPY . .

# ---------- Runtime stage ----------
FROM node:20-alpine
WORKDIR /app
COPY --from=builder /app .
EXPOSE 5001
CMD ["node", "index.js"]

